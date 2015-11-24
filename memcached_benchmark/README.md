Memcached's client for benchmarking and testing.

The innovation in the following client is that if a connection with Memcached's server is lost, the client tries to continue the caching (both sending and retrieving data) with another server, and if it also fails, then it tries to continue with a third server. That means that if the data is backed up in another two servers, the client can continue to work seamlessly (with only a small delay for establishing new connection), without adding cache misses.

The benchmark shows regular cache misses, together with total misses - i.e. the misses that happen when the server falls, and the relevant data is not yet backed up in another server.

The following client is a modification of CloudSuite's client, and those is distributed under the same licence. Please see the licence below.
The modification of CloudSuite's client was developed by Samyon Ristov at Hebrew University of Jerusalem, under the supervision of Prof. Danny Dolev, Tal Anker and Yaron Weinsberg.

Original benchmark:
http://parsa.epfl.ch/cloudsuite/memcached.html
Link to original license:
http://parsa.epfl.ch/cloudsuite/licenses.html

Licence:
CloudSuite 2.0 License

CloudSuite 2.0 Benchmark Suite
Copyright (c) 2011-2013, Parallel Systems Architecture Lab, EPFL
All rights reserved.
Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

    Redistributions of source code must retain the above copyright
    notice, this list of conditions and the following disclaimer.
    Redistributions in binary form must reproduce the above copyright
    notice, this list of conditions and the following disclaimer in the
    documentation and/or other materials provided with the distribution.
    Neither the name of the Parallel Systems Architecture Laboratory, EPFL,
    nor the names of its contributors may be used to endorse or promote
    products derived from this software without specific prior written permission.

    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE PARALLEL SYSTEMS ARCHITECTURE LABORATORY, EPFL BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.