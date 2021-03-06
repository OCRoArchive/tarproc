
# Module `tarproclib.paths`

```
Help on module tarproclib.paths in tarproclib:

NAME
    tarproclib.paths

DESCRIPTION
    # Copyright (c) 2017-2019 NVIDIA CORPORATION. All rights reserved.
    # This file is part of webloader (see TBD).
    # See the LICENSE file for licensing terms (BSD-style).
    #

CLASSES
    builtins.object
        ChDir
        DirPlusFile
        FilePlusExt
    
    class ChDir(builtins.object)
     |  ChDir(path)
     |  
     |  Methods defined here:
     |  
     |  __enter__(self)
     |  
     |  __exit__(self, *args)
     |  
     |  __init__(self, path)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)
    
    class DirPlusFile(builtins.object)
     |  DirPlusFile(path)
     |  
     |  Methods defined here:
     |  
     |  __init__(self, path)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  base(self)
     |  
     |  key(self)
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)
    
    class FilePlusExt(builtins.object)
     |  FilePlusExt(path)
     |  
     |  Methods defined here:
     |  
     |  __init__(self, path)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  base(self)
     |  
     |  key(self)
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)

FUNCTIONS
    base_plus_ext(path)
        Helper method that splits off all extension.
        
        Returns base, allext.
        
        :param path: path with extensions
        :returns: path with all extensions removed
    
    dir_plus_file(path)
        Helper method that splits off all extension.
        
        Returns base, allext.
        
        :param path: path with extensions
        :returns: path with all extensions removed
    
    filebase(fname)
    
    fullext(fname)
    
    read_binary(fname)
    
    write_binary(fname, data)

FILE
    /home/tmb/proj/tarproc/tarproclib/paths.py



```

# Module `tarproclib.gopen`

```
Help on module tarproclib.gopen in tarproclib:

NAME
    tarproclib.gopen

DESCRIPTION
    # Copyright (c) 2017-2019 NVIDIA CORPORATION. All rights reserved.
    # This file is part of webloader (see TBD).
    # See the LICENSE file for licensing terms (BSD-style).
    #

CLASSES
    builtins.Exception(builtins.BaseException)
        GopenException
    builtins.object
        Pipe
    
    class GopenException(builtins.Exception)
     |  GopenException(info)
     |  
     |  Common base class for all non-exit exceptions.
     |  
     |  Method resolution order:
     |      GopenException
     |      builtins.Exception
     |      builtins.BaseException
     |      builtins.object
     |  
     |  Methods defined here:
     |  
     |  __init__(self, info)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)
     |  
     |  ----------------------------------------------------------------------
     |  Static methods inherited from builtins.Exception:
     |  
     |  __new__(*args, **kwargs) from builtins.type
     |      Create and return a new object.  See help(type) for accurate signature.
     |  
     |  ----------------------------------------------------------------------
     |  Methods inherited from builtins.BaseException:
     |  
     |  __delattr__(self, name, /)
     |      Implement delattr(self, name).
     |  
     |  __getattribute__(self, name, /)
     |      Return getattr(self, name).
     |  
     |  __reduce__(...)
     |      Helper for pickle.
     |  
     |  __repr__(self, /)
     |      Return repr(self).
     |  
     |  __setattr__(self, name, value, /)
     |      Implement setattr(self, name, value).
     |  
     |  __setstate__(...)
     |  
     |  __str__(self, /)
     |      Return str(self).
     |  
     |  with_traceback(...)
     |      Exception.with_traceback(tb) --
     |      set self.__traceback__ to tb and return self.
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors inherited from builtins.BaseException:
     |  
     |  __cause__
     |      exception cause
     |  
     |  __context__
     |      exception context
     |  
     |  __dict__
     |  
     |  __suppress_context__
     |  
     |  __traceback__
     |  
     |  args
    
    class Pipe(builtins.object)
     |  Pipe(*args, raise_errors=True, **kw)
     |  
     |  Methods defined here:
     |  
     |  __enter__(self)
     |  
     |  __exit__(self, type, value, traceback)
     |  
     |  __init__(self, *args, raise_errors=True, **kw)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  close(self)
     |  
     |  open(self, *args, **kw)
     |  
     |  read(self, *args, **kw)
     |  
     |  readLine(self, *args, **kw)
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)

FUNCTIONS
    gopen(url, mode='rb')
        Open a stream using different handlers.
        
        :param url: url to be opened
        :param mode: read or write

DATA
    bufsize = 8192
    handlers = {'file': "dd if='{}' bs=4M", 'gs': "gsutil cat '{}'", 'http...
    prefix = 'GOPEN_'

FILE
    /home/tmb/proj/tarproc/tarproclib/gopen.py



```

# Module `tarproclib.writer`

```
Help on module tarproclib.writer in tarproclib:

NAME
    tarproclib.writer

DESCRIPTION
    # Copyright (c) 2017-2019 NVIDIA CORPORATION. All rights reserved.
    # This file is part of webloader (see TBD).
    # See the LICENSE file for licensing terms (BSD-style).
    #

CLASSES
    builtins.object
        TarWriter1
    
    class TarWriter1(builtins.object)
     |  TarWriter1(fileobj, keep_meta=False, user='bigdata', group='bigdata', mode=292, compress=None, encoder=None, output_mode=None)
     |  
     |  Methods defined here:
     |  
     |  __enter__(self)
     |  
     |  __exit__(self, exc_type, exc_val, exc_tb)
     |  
     |  __init__(self, fileobj, keep_meta=False, user='bigdata', group='bigdata', mode=292, compress=None, encoder=None, output_mode=None)
     |      A class for writing dictionaries to tar files.
     |      
     |      :param fileobj: fileobj: file name for tar file (.tgz)
     |      :param bool: keep_meta: keep fields starting with "_"
     |      :param keep_meta:  (Default value = False)
     |      :param encoder: sample encoding (Default value = None)
     |      :param compress:  (Default value = None)
     |  
     |  close(self)
     |      Close the tar file.
     |  
     |  write(self, obj)
     |      Write a dictionary to the tar file.
     |      
     |      :param obj: dictionary of objects to be stored
     |      :returns: size of the entry
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)

FUNCTIONS
    TarWriter(url, **kw)
        Write either to a URL or a ZMQ stream.
        
        :param url: output URL
        :param **kw: other parameters

DATA
    __all__ = ['TarWriter1', 'TarWriter']

FILE
    /home/tmb/proj/tarproc/tarproclib/writer.py



```

# Module `tarproclib.zcom`

```
Help on module tarproclib.zcom in tarproclib:

NAME
    tarproclib.zcom

DESCRIPTION
    # Copyright (c) 2017-2019 NVIDIA CORPORATION. All rights reserved.
    # This file is part of webloader (see TBD).
    # See the LICENSE file for licensing terms (BSD-style).
    #

CLASSES
    builtins.object
        Connection
        MultiWriter
    
    class Connection(builtins.object)
     |  Connection(urls=None, noexpand=False, keep_meta=True, **kw)
     |  
     |  A class for sending/receiving samples via ZMQ sockets.
     |  
     |  Methods defined here:
     |  
     |  __enter__(self)
     |  
     |  __exit__(self, exc_type, exc_val, exc_tb)
     |  
     |  __init__(self, urls=None, noexpand=False, keep_meta=True, **kw)
     |      Initialize a connection.
     |      
     |      :param urls:  list of ZMQ-URL to connect to (Default value = None)
     |      :param noexpand: do not expand braces in URLs (Default value = False)
     |  
     |  __iter__(self, report=-1)
     |      Receive data through an iterator
     |  
     |  close(self, linger=-1)
     |      Close the connection.
     |  
     |  connect(self, urls, topic='', noexpand=False)
     |  
     |  recv(self)
     |      Receive data from the connection.
     |  
     |  send(self, sample)
     |      Send data over the connection.
     |      
     |      :param sample: sample to be sent
     |  
     |  send_eof(self)
     |  
     |  write(self, sample)
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)
    
    class MultiWriter(builtins.object)
     |  MultiWriter(urls=None, noexpand=False, keep_meta=True, linger=-1, output_mode='random', **kw)
     |  
     |  A class for sending/receiving samples via ZMQ sockets.
     |  
     |  Methods defined here:
     |  
     |  __enter__(self)
     |  
     |  __exit__(self, exc_type, exc_val, exc_tb)
     |  
     |  __init__(self, urls=None, noexpand=False, keep_meta=True, linger=-1, output_mode='random', **kw)
     |      Initialize a connection.
     |      
     |      :param urls:  list of ZMQ-URL to connect to (Default value = None)
     |      :param noexpand: do not expand braces in URLs (Default value = False)
     |  
     |  close(self, linger=-1)
     |      Close the connection.
     |  
     |  connect(self, urls, topic='', noexpand=False)
     |  
     |  send(self, sample)
     |      Send data over the connection.
     |      
     |      :param sample: sample to be sent
     |  
     |  send_eof(self)
     |  
     |  write(self, sample)
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)

FUNCTIONS
    urls2list(urls, noexpand=False)
    
    zmq_connect(socket, urls, topic='')
        Explicitly connect to a ZMQ socket.
        
        :param url: ZMQ-URL to connect to  (Default value = "")
        :param topic: topic to subscribe to for SUB sockets (Default value = "")
    
    zmq_make(context, url, linger=0)
        Make a ZMQ socket for a context and url.
        
        :param context: context
        :param url: target URL
        :param linger: linger flag

DATA
    schemes = {'zpub': (1, True), 'zpull': (7, True), 'zpush': (8, False),...
    verbose = 1

FILE
    /home/tmb/proj/tarproc/tarproclib/zcom.py



```

# Module `tarproclib.proc`

```
Help on module tarproclib.proc in tarproclib:

NAME
    tarproclib.proc

DESCRIPTION
    # Copyright (c) 2017-2019 NVIDIA CORPORATION. All rights reserved.
    # This file is part of webloader (see TBD).
    # See the LICENSE file for licensing terms (BSD-style).
    #

FUNCTIONS
    ishuffle(data, bufsize=1000, initial=100)
        Shuffle the data in the stream.
        
        This uses a buffer of size `bufsize`. Shuffling at
        startup is less random; this is traded off against
        yielding samples quickly.
        
        :param data: iterator
        :param bufsize: buffer size for shuffling
        :returns: iterator

FILE
    /home/tmb/proj/tarproc/tarproclib/proc.py



```

# Module `tarproclib.reader`

```
Help on module tarproclib.reader in tarproclib:

NAME
    tarproclib.reader

DESCRIPTION
    # Copyright (c) 2017-2019 NVIDIA CORPORATION. All rights reserved.
    # This file is part of webloader (see TBD).
    # See the LICENSE file for licensing terms (BSD-style).
    #

CLASSES
    builtins.object
        TarIterator1
    
    class TarIterator1(builtins.object)
     |  TarIterator1(url, braceexpand=True, shuffle=False, allow_missing=False, **kw)
     |  
     |  Iterate of tar files consisting of samples.
     |  
     |  :param url: source URL
     |  :param braceexpand: expand braces in the source URL
     |  :param shuffle: shuffle the samples
     |  :param allow_missing: allow missing shards
     |  :param **kw:
     |  
     |  Methods defined here:
     |  
     |  __init__(self, url, braceexpand=True, shuffle=False, allow_missing=False, **kw)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  __iter__(self)
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)

FUNCTIONS
    TarIterator(url, **kw)
        Open an iterator of tar files.
        
        This can open either ZMQ URLs or object store URLs.
        
        :param url: source URL
        :param **kw:
    
    tariterator(fileobj, keys=<function base_plus_ext at 0x7f43ba9b2050>, decoder=None, suffixes=None, errors=True, container=None)
        Iterate through training samples stored in a sharded tar file.
        
        :param fileobj:
        :param check_sorted:  (Default value = False)
        :param keys:  (Default value = base_plus_ext)
        :param decode:  (Default value = True)

DATA
    __all__ = ['tariterator', 'TarIterator1', 'TarIterator']

FILE
    /home/tmb/proj/tarproc/tarproclib/reader.py



```
