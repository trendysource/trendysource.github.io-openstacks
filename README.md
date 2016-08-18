# trendysource.github.io-openstacks
openstack
keystone-all

os.path:

DESCRIPTION:
Instead of importing this module directly, import os and refer to
    this module as os.path.  The "os.path" name is an alias for this
    module on Posix systems; on other systems (e.g. Mac, Windows),
    os.path provides the same operations in a manner specific to that
    platform, and is an alias to another module (e.g. macpath, ntpath).
    
    Some of this can actually be useful on non-Posix systems too, e.g.
    for manipulation of the pathname component of URLs.
	
FUNCTIONS
    abspath(path)
        Return an absolute path. # 返回一个绝对路径
    
    basename(p)
        Returns the final component of a pathname
    
    commonprefix(m)
        Given a list of pathnames, returns the longest common leading component
    
    dirname(p)
        Returns the directory component of a pathname
    
    exists(path)
        Test whether a path exists.  Returns False for broken symbolic links
    
    expanduser(path)
        Expand ~ and ~user constructions.  If user or $HOME is unknown,
        do nothing.
    
    expandvars(path)
        Expand shell variables of form $var and ${var}.  Unknown variables
        are left unchanged.
    
    getatime(filename)
        Return the last access time of a file, reported by os.stat().
    
    getctime(filename)
        Return the metadata change time of a file, reported by os.stat().
    
    getmtime(filename)
        Return the last modification time of a file, reported by os.stat().
    
    getsize(filename)
        Return the size of a file, reported by os.stat().
    
    isabs(s)
        Test whether a path is absolute
    
    isdir(s)
        Return true if the pathname refers to an existing directory.
    
    isfile(path)
        Test whether a path is a regular file
    
    islink(path)
        Test whether a path is a symbolic link
    
    ismount(path)
        Test whether a path is a mount point
    
    join(a, *p)
        Join two or more pathname components, inserting '/' as needed.
        If any component is an absolute path, all previous path components
        will be discarded.  An empty last part will result in a path that
        ends with a separator.
    
    lexists(path)
        Test whether a path exists.  Returns True for broken symbolic links
    
    normcase(s)
        Normalize case of pathname.  Has no effect under Posix
    
    normpath(path)
        Normalize path, eliminating double slashes, etc.
    
    realpath(filename)
        Return the canonical path of the specified filename, eliminating any
        symbolic links encountered in the path.
    
    relpath(path, start='.')
        Return a relative version of a path
    
    samefile(f1, f2)
        Test whether two pathnames reference the same actual file
    
    sameopenfile(fp1, fp2)
        Test whether two open file objects reference the same file
    
    samestat(s1, s2)
        Test whether two stat buffers reference the same file
    
    split(p)
        Split a pathname.  Returns tuple "(head, tail)" where "tail" is
        everything after the final slash.  Either part may be empty.
    
    splitdrive(p)
        Split a pathname into drive and path. On Posix, drive is always
        empty.
    
    splitext(p)
        Split the extension from a pathname.
        
        Extension is everything from the last dot to the end, ignoring
        leading dots.  Returns "(root, ext)"; ext may be empty.
    
    walk(top, func, arg)
        Directory tree walk with callback function.
        
        For each directory in the directory tree rooted at top (including top
        itself, but excluding '.' and '..'), call func(arg, dirname, fnames).
        dirname is the name of the directory, and fnames a list of the names of
        the files and subdirectories in dirname (excluding '.' and '..').  func
        may modify the fnames list in-place (e.g. via del or slice assignment),
        and walk will only recurse into the subdirectories whose names remain in
        fnames; this can be used to implement a filter, or to impose a specific
        order of visiting.  No semantics are defined for, or required of, arg,
        beyond that arg is always passed to func.  It can be used, e.g., to pass
        a filename pattern, or a mutable object designed to accumulate
        statistics.  Passing None for arg is common.

DATA
    __all__ = ['normcase', 'isabs', 'join', 'splitdrive', 'split', 'splite...
    altsep = None
    curdir = '.' # 获取当前目录的字符串名
    defpath = ':/bin:/usr/bin'
    devnull = '/dev/null'
    extsep = '.'
    pardir = '..'   # os.pardir  获取当前目录的父目录字符串名：('..')
    pathsep = ':'
    sep = '/'
    supports_unicode_filenames = False
	
os.path.abspath(path) #返回绝对路径
os.path.basename(path) #返回文件名
os.path.commonprefix(list) #返回list(多个路径)中，所有path共有的最长的路径。
os.path.dirname(path) #返回文件路径
os.path.exists(path)  #路径存在则返回True,路径损坏返回False
os.path.lexists  #路径存在则返回True,路径损坏也返回True
os.path.expanduser(path)  #把path中包含的"~"和"~user"转换成用户目录
os.path.expandvars(path)  #根据环境变量的值替换path中包含的”$name”和”${name}”
os.path.getatime(path)  #返回最后一次进入此path的时间。
os.path.getmtime(path)  #返回在此path下最后一次修改的时间。
os.path.getctime(path)  #返回path的大小
os.path.getsize(path)  #返回文件大小，如果文件不存在就返回错误
os.path.isabs(path)  #判断是否为绝对路径
os.path.isfile(path)  #判断路径是否为文件
os.path.isdir(path)  #判断路径是否为目录
os.path.islink(path)  #判断路径是否为链接
os.path.ismount(path)  #判断路径是否为挂载点（）
os.path.join(path1[, path2[, ...]])  #把目录和文件名合成一个路径
os.path.normcase(path)  #转换path的大小写和斜杠
os.path.normpath(path)  #规范path字符串形式
os.path.realpath(path)  #返回path的真实路径
os.path.relpath(path[, start])  #从start开始计算相对路径
os.path.samefile(path1, path2)  #判断目录或文件是否相同
os.path.sameopenfile(fp1, fp2)  #判断fp1和fp2是否指向同一文件
os.path.samestat(stat1, stat2)  #判断stat tuple stat1和stat2是否指向同一个文件
os.path.split(path)  #把路径分割成dirname和basename，返回一个元组
os.path.splitdrive(path)   #一般用在windows下，返回驱动器名和路径组成的元组
os.path.splitext(path)  #分割路径，返回路径名和文件扩展名的元组
os.path.splitunc(path)  #把路径分割为加载点与文件
os.path.walk(path, visit, arg)  #遍历path，进入每个目录都调用visit函数，visit函数必须有
3个参数(arg, dirname, names)，dirname表示当前目录的目录名，names代表当前目录下的所有
文件名，args则为walk的第三个参数
os.path.supports_unicode_filenames  #设置是否支持unicode路径名	

##################################################################################### 
os.path:
Help on list object:

class list(object)
 |  list() -> new empty list
 |  list(iterable) -> new list initialized from iterable's items
 |  
 |  Methods defined here:
 |  
 |  __add__(...)
 |      x.__add__(y) <==> x+y
 |  
 |  __contains__(...)
 |      x.__contains__(y) <==> y in x
 |  
 |  __delitem__(...)
 |      x.__delitem__(y) <==> del x[y]
 |  
 |  __delslice__(...)
 |      x.__delslice__(i, j) <==> del x[i:j]
 |      
 |      Use of negative indices is not supported.
 |  
 |  __eq__(...)
 |      x.__eq__(y) <==> x==y
 |  
 |  __ge__(...)
 |      x.__ge__(y) <==> x>=y
 |  
 |  __getattribute__(...)
 |      x.__getattribute__('name') <==> x.name
 |  
 |  __getitem__(...)
 |      x.__getitem__(y) <==> x[y]
 |  
 |  __getslice__(...)
 |      x.__getslice__(i, j) <==> x[i:j]
 |      
 |      Use of negative indices is not supported.
 |  
 |  __gt__(...)
 |      x.__gt__(y) <==> x>y
 |  
 |  __iadd__(...)
 |      x.__iadd__(y) <==> x+=y
 |  
 |  __imul__(...)
 |      x.__imul__(y) <==> x*=y
 |  
 |  __init__(...)
 |      x.__init__(...) initializes x; see help(type(x)) for signature
 |  
 |  __iter__(...)
 |      x.__iter__() <==> iter(x)
 |  
 |  __le__(...)
 |      x.__le__(y) <==> x<=y
 |  
 |  __len__(...)
 |      x.__len__() <==> len(x)
 |  
 |  __lt__(...)
 |      x.__lt__(y) <==> x<y
 |  
 |  __mul__(...)
 |      x.__mul__(n) <==> x*n
 |  
 |  __ne__(...)
 |      x.__ne__(y) <==> x!=y
 |  
 |  __repr__(...)
 |      x.__repr__() <==> repr(x)
 |  
 |  __reversed__(...)
 |      L.__reversed__() -- return a reverse iterator over the list
 |  
 |  __rmul__(...)
 |      x.__rmul__(n) <==> n*x
 |  
 |  __setitem__(...)
 |      x.__setitem__(i, y) <==> x[i]=y
 |  
 |  __setslice__(...)
 |      x.__setslice__(i, j, y) <==> x[i:j]=y
 |      
 |      Use  of negative indices is not supported.
 |  
 |  __sizeof__(...)
 |      L.__sizeof__() -- size of L in memory, in bytes
 |  
 |  append(...)
 |      L.append(object) -- append object to end
 |  
 |  count(...)
 |      L.count(value) -> integer -- return number of occurrences of value
 |  
 |  extend(...)
 |      L.extend(iterable) -- extend list by appending elements from the iterable
 |  
 |  index(...)
 |      L.index(value, [start, [stop]]) -> integer -- return first index of value.
 |      Raises ValueError if the value is not present.
 |  
 |  insert(...)
 |      L.insert(index, object) -- insert object before index
 |  
 |  pop(...)
 |      L.pop([index]) -> item -- remove and return item at index (default last).
 |      Raises IndexError if list is empty or index is out of range.
 |  
 |  remove(...)
 |      L.remove(value) -- remove first occurrence of value.
 |      Raises ValueError if the value is not present.
 |  
 |  reverse(...)
 |      L.reverse() -- reverse *IN PLACE*
 |  
 |  sort(...)
 |      L.sort(cmp=None, key=None, reverse=False) -- stable sort *IN PLACE*;
 |      cmp(x, y) -> -1, 0, 1
 |  
 |  ----------------------------------------------------------------------
 |  Data and other attributes defined here:
 |  
 |  __hash__ = None
 |  
 |  __new__ = <built-in method __new__ of type object>
 |      T.__new__(S, ...) -> a new object with type S, a subtype of T

