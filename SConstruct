###
#env = Environment(CPPPATH=['/home/guang/yan/msquic/src/inc', '/home/guang/yan/msquic/build/_deps/opensslquic-build/openssl/include'])
env = Environment(CPPPATH=['/home/guang/yan/msquic/src/inc', '/home/guang/yan/wolfssl-5.6.6/wolfssl', '/home/guang/yan/wolfssl-5.6.6'])
#env.Append(CCFLAGS=['-O3', '-DNDEBUG', '-fms-extensions', '-fPIC', '-Wno-multichar', '-Wall', '-Wextra'])
env.Append(CCFLAGS=['-O3', '-DNDEBUG', '-fms-extensions', '-fPIC', '-Wno-multichar', '-Werror'])
env.Append(CPPDEFINES = ['CX_PLATFORM_LINUX', 'HAS_SENDMMSG', 'HAS_SYSCONF', 'HAS__SC_PHYS_PAGES', 'QUIC_ENABLE_CA_CERTIFICATE_FILE_TESTS'])
env.Append(CPPDEFINES = ['QUIC_EVENTS_STUB', 'QUIC_LOGS_STUB', 'QUIC_SHARED_EPHEMERAL_WORKAROUND', 'QUIC_TEST_OPENSSL_FLAGS=1'])
env.Append(CPPDEFINES = ['VER_BUILD_ID=0', 'VER_GIT_HASH=86e08e5bc9c593f27d2981c5f85bff087977859c', 'VER_SUFFIX=-private', '_GNU_SOURCE'])
env.Append(LIBS = ['pthread', 'dl', 'm'])
# ./src/crypto/tls_openssl.c
# ./src/crypto/crypto_openssl.c

src_files = Split("""
src/core/ack_tracker.c
src/core/api.c
src/core/binding.c
src/core/configuration.c
src/core/congestion_control.c
src/core/connection.c
src/core/crypto.c
src/core/crypto_tls.c
src/core/cubic.c
src/core/bbr.c
src/core/datagram.c
src/core/frame.c
src/core/library.c
src/core/listener.c
src/core/lookup.c
src/core/loss_detection.c
src/core/mtu_discovery.c
src/core/operation.c
src/core/packet.c
src/core/packet_builder.c
src/core/packet_space.c
src/core/path.c
src/core/range.c
src/core/recv_buffer.c
src/core/registration.c
src/core/send.c
src/core/send_buffer.c
src/core/sent_packet_metadata.c
src/core/settings.c
src/core/stream.c
src/core/stream_recv.c
src/core/stream_send.c
src/core/stream_set.c
src/core/timer_wheel.c
src/core/worker.c
src/core/version_neg.c
src/core/sliding_window_extremum.c
src/core/inline.c
./src/platform/crypt.c
./src/platform/hashtable.c
./src/platform/pcp.c
./src/platform/platform_worker.c
./src/platform/toeplitz.c
./src/platform/inline.c
./src/platform/platform_posix.c
./src/platform/storage_posix.c
./src/platform/cgroup.c
./src/platform/datapath_raw_linux.c
./src/platform/datapath_raw_socket.c
./src/platform/datapath_raw_socket_linux.c
./src/platform/datapath_raw_xdp_linux.c
./src/platform/datapath_epoll.c
./src/platform/datapath_linux.c
./src/platform/tls_openssl.c
./src/platform/crypt_openssl.c
./src/platform/certificates_posix.c
./src/platform/selfsign_openssl.c
./src/bin/linux/init.c
./src/tools/sample/sample.c
""")

#env.Program('msquic', src_files)
env.Program('msquic', [src_files, '/home/guang/yan/wolfssl-5.6.6/src/.libs/libwolfssl.a'])
#env.Program('msquic', [src_files, '/home/guang/yan/msquic/build/_deps/opensslquic-build/openssl/lib/libssl.a', '/home/guang/yan/msquic/build/_deps/opensslquic-build/openssl/lib/libcrypto.a'])


