#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.68])
AC_INIT([libqatengine], [1.0], [])
AC_CONFIG_SRCDIR([config.h.in])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_AUX_DIR([.])
AM_INIT_AUTOMAKE([foreign])

#Libtool for generating shared library
LT_INIT
AC_PROG_LIBTOOL
AC_PROG_LN_S
AC_CONFIG_MACRO_DIR([m4])

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC

# Parameter parsing for disabling the feature
AC_ARG_ENABLE(qat_rsa,
              AS_HELP_STRING([--disable-qat_rsa],
                             [Disable accelerated RSA offload]))
AC_SUBST(enable_qat_rsa)

AC_ARG_ENABLE(qat_ciphers,
              AS_HELP_STRING([--disable-qat_ciphers],
                             [Disable accelerated CIPHERS offload]))
AC_SUBST(enable_qat_ciphers)

AC_ARG_ENABLE(qat_ecdh,
              AS_HELP_STRING([--disable-qat_ecdh],
                             [Disable accelerated ECDH offload]))
AC_SUBST(enable_qat_ecdh)

AC_ARG_ENABLE(qat_ecdsa,
              AS_HELP_STRING([--disable-qat_ecdsa],
                             [Disable accelerated ECDSA offload]))
AC_SUBST(enable_qat_ecdsa)

AC_ARG_ENABLE(qat_dsa,
              AS_HELP_STRING([--disable-qat_dsa],
                             [Disable accelerated DSA offload]))
AC_SUBST(enable_qat_dsa)

AC_ARG_ENABLE(qat_dh,
              AS_HELP_STRING([--disable-qat_dh],
                             [Disable accelerated DH offload]))
AC_SUBST(enable_qat_dh)

AC_ARG_ENABLE(qat_prf,
              AS_HELP_STRING([--disable-qat_prf],
                             [Disable accelerated PRF offload]))
AC_SUBST(enable_qat_prf)

AC_ARG_ENABLE(qat_hkdf,
              AS_HELP_STRING([--enable-qat_hkdf],
                             [Enable accelerated HKDF offload]))
AC_SUBST(enable_qat_hkdf)

AC_ARG_ENABLE(qat_ecx,
              AS_HELP_STRING([--disable-qat_ecx],
                             [Disable accelerated X25519/X448 offload]))
AC_SUBST(enable_qat_ecx)

AC_ARG_ENABLE(vaes_gcm,
              AS_HELP_STRING([--disable-vaes_gcm],
                             [Disable vectorized AES-GCM offload]))
AC_SUBST(enable_vaes_gcm)

AC_ARG_ENABLE(multibuff_rsa,
              AS_HELP_STRING([--disable-multibuff_rsa],
                             [Disable multibuff RSA offload]))
AC_SUBST(enable_multibuff_rsa)

AC_ARG_ENABLE(multibuff_ecx,
              AS_HELP_STRING([--disable-multibuff_ecx],
                             [Disable multibuff X25519 offload]))
AC_SUBST(enable_multibuff_ecx)

AC_ARG_ENABLE(qat_small_pkt_offload,
              AS_HELP_STRING([--enable-qat_small_pkt_offload],
                             [Enable accelerated small packet CIPHER offload]))
AC_SUBST(enable_qat_small_pkt_offload)

AC_ARG_ENABLE(qat_offload,
              AS_HELP_STRING([--disable-qat_offload],
                             [Disable Intel(R) QAT Hardware offload]))
AC_SUBST(enable_qat_offload)

AC_ARG_ENABLE(multibuff_offload,
              AS_HELP_STRING([--enable-multibuff_offload],
                             [Enable Multibuff offload using Intel(R) Crypto Multi-buffer library]))
AC_SUBST(enable_multibuff_offload)

AC_ARG_ENABLE(ipsec_offload,
              AS_HELP_STRING([--enable-ipsec_offload],
                             [Enable VAES GCM offload]))
AC_SUBST(ipsec_offload)

# Parameter parsing for self tuning of the timeout in the multibuff polling thread
AC_ARG_ENABLE(multibuff_heuristic_timeout,
              AS_HELP_STRING([--enable-multibuff_heuristic_timeout],
                             [Enable self tuning of the timeout in the multibuff polling thread]))
AC_SUBST(enable_multibuff_heuristic_timeout)

AC_ARG_ENABLE(qat_cycle_counts,
              AS_HELP_STRING([--enable-qat_cycle_counts],
                             [Enable CPU Cycle Counts]))
AC_SUBST(enable_qat_cycle_counts)

# Parameter parsing for enabling debug/warnings
AC_ARG_ENABLE(qat_debug,
              AS_HELP_STRING([--enable-qat_debug],
                             [Enable Engine Debug Messages]))
AC_SUBST(enable_qat_debug)

AC_ARG_ENABLE(qat_warnings,
              AS_HELP_STRING([--enable-qat_warnings],
                             [Enable Engine Warning Messages]))
AC_SUBST(enable_qat_warnings)

AC_ARG_ENABLE(qat_mem_debug,
              AS_HELP_STRING([--enable-qat_mem_debug],
                             [Enable Memory Driver Debug Messages]))
AC_SUBST(enable_qat_mem_debug)

AC_ARG_ENABLE(qat_mem_warnings,
              AS_HELP_STRING([--enable-qat_mem_warnings],
                             [Enable Memory Driver Warning Messages]))
AC_SUBST(enable_qat_mem_warnings)

# Mandatory QAT driver source path if building against 1.7 driver source package
AC_ARG_WITH(qat_dir,
              AS_HELP_STRING([--with-qat_dir],
                             [Path to the Intel Quickassist Technology Driver source code]))
AC_SUBST(with_qat_dir)

# Other non mandatory parameters
AC_ARG_WITH(openssl_install_dir,
              AS_HELP_STRING([--with-openssl_install_dir],
                             [Path to where the OpenSSL libraries are installed to. The Engine will be installed to the lib/engines subdirectory of this path]))
AC_SUBST(with_openssl_install_dir)

AC_ARG_WITH(openssl_dir,
              AS_HELP_STRING([--with-openssl_dir],
                             [Path to the OpenSSL source code. The error files will get regenerated using the mkerr.pl script included with the OpenSSL source]))
AC_SUBST(with_openssl_dir)

AC_ARG_WITH(qat_install_dir,
              AS_HELP_STRING([--with-qat_install_dir],
                             [Path to the Intel Quickassist Technology Driver build output]))
AC_SUBST(with_qat_install_dir)

AC_ARG_WITH(multibuff_install_dir,
              AS_HELP_STRING([--with-multibuff_install_dir],
                             [Path to the Multi-buffer based Intel(R) Crypto Multi-buffer library build output]))
AC_SUBST(with_multibuff_install_dir)

AC_ARG_WITH(ipsec_install_dir,
            AS_HELP_STRING([--with-ipsec_install_dir],
                           [Path to the VAES based Intel(R) IPSec library build output]))
AC_SUBST(with_ipsec_install_dir)

AC_ARG_ENABLE(qat_contig_mem,
              AS_HELP_STRING([--enable-qat_contig_mem],
                             [This should be specified to force the Engine to use the qat_contig_mem component supplied within the QAT Engine release package]))
AC_SUBST(enable_qat_contig_mem)

AC_ARG_WITH(usdm_dir,
              AS_HELP_STRING([--with-usdm_dir],
                             [Path to the USDM Component source code. This should be used to specify a path to the USDM Component source other than the standard default path within the QAT1.7 Intel Quickassist Technology Driver source code]))
AC_SUBST(with_usdm_dir)

AC_ARG_WITH(qat_debug_file,
              AS_HELP_STRING([--with-qat_debug_file],
                             [Path and filename to log debug output to. Combine with other flags that enable the debug and warning output]))
AC_SUBST(with_qat_debug_file)

AC_ARG_WITH(qat_engine_id,
              AS_HELP_STRING([--with-qat_engine_id],
                             [This should be specified to force the Engine to use engine id other than default "qatengine"]))
AC_SUBST(with_qat_engine_id)

AC_ARG_WITH(cc_opt,
              AS_HELP_STRING([--with-cc_opt],
                             [Sets additional parameters that will be added to the CFLAGS]))
AC_SUBST(with_cc_opt)

AC_ARG_WITH(ld_opt,
              AS_HELP_STRING([--with-ld_opt],
                             [Sets additional parameters that will be used during linking]))
AC_SUBST(with_ld_opt)

AC_ARG_ENABLE(multi_thread,
            AS_HELP_STRING([--enable-multi_thread],
                           [Enable using a multi threaded version of the user space part of the supplied memory driver. Please see the documentation on limitations of using this option]))
AC_SUBST(enable_multi_thread)

AC_ARG_ENABLE(qat_lenstra_protection,
              AS_HELP_STRING([--disable-qat_lenstra_protection],
                             [Disable protection against Lenstra attack]))
AC_SUBST(enable_qat_lenstra_protection)

AC_ARG_ENABLE(qat_auto_engine_init_on_fork,
              AS_HELP_STRING([--disable-qat_auto_engine_init_on_fork],
                             [Disable auto initialization of the engine following a fork]))
AC_SUBST(enable_qat_auto_engine_init_on_fork)

if test "x$with_qat_dir" = "x"
then
  AC_CHECK_FILE(/usr/include/qat/icp_sal_versions.h, , [])
  if test "x$ac_cv_file__usr_include_qat_icp_sal_versions_h" = "xyes"
  then
    if test `grep "define SAL_INFO2_DRIVER_SW_VERSION_TYPE \"in-tree\"" /usr/include/qat/icp_sal_versions.h | wc -l` = "1"
    then
      AC_SUBST(cflags_qat_intree, "-DQAT_DRIVER_INTREE -DQAT_DISABLE_NONZERO_MEMFREE")
      AC_SUBST(with_qat_dir, "/usr/lib64")
      AC_MSG_NOTICE([QAT intree driver using QATlib RPM])
    fi
  fi
fi

# ERROR message if mandatory options are not provided
if test "x$cflags_qat_intree" = "x"
then
  if test "x$with_qat_dir" = "x" -a "x$enable_multibuff_offload" = "x" -a  "x$enable_ipsec_offload" = "x"
  then
    AC_MSG_ERROR([--with-qat_dir or --enable-multibuff_offload or --enable-ipsec_offload not set, If you like to use QAT offload, set it to the path to the Intel Quickassist Technology Driver source code. e.g: --with-qat_dir=/path/to/qat_driver or If you like to use Multi-buffer Software offload using Intel crypto_mb, enable using --enable-multibuff_offload or if you like to use Intel IPSec offload, enable using --enable-ipsec_offload.])
  fi
fi

# OpenSSL install dir or set system openssl install dir if not provided
if test "x$with_openssl_install_dir" != "x"
then
  ac_default_prefix=$with_openssl_install_dir
  if test "`grep "define OPENSSL_VERSION_MAJOR" $with_openssl_install_dir/include/openssl/opensslv.h | awk '{print $4}'`" = "3"
  then
    AC_MSG_NOTICE([Build QAT engine against OpenSSL 3.0.0])
    AC_ARG_WITH(cflags_openssl_300, AS_HELP_STRING(), , cflags_openssl_300="-DSSL_QAT_USE_ASYNC_CALLBACK")
    AC_SUBST(cflags_openssl_300)
    engine_install_dir="\$(with_openssl_install_dir)/lib/engines-3"
  else
    AC_MSG_NOTICE([Build QAT engine against OpenSSL 1.1.x])
    engine_install_dir="\$(with_openssl_install_dir)/lib/engines-1.1"
    if test "`grep "define OPENSSL_VERSION_NUMBER  0x10100" $with_openssl_install_dir/include/openssl/opensslv.h | wc -l`" = "1"
    then
      if test "x$with_openssl_dir" = "x"
      then
        AC_MSG_ERROR([OpenSSL version 1.1.0! Additional flag "--with-openssl_dir" pointing to the OpenSSL source dir needs to be configured for OpenSSL 1.1.0 to regenerate err files])
      fi
      AC_ARG_WITH(cflags_openssl_110, AS_HELP_STRING(), , cflags_openssl_110="-DQAT_OPENSSL_110")
      AC_SUBST(cflags_openssl_110)
    fi
  fi
  AC_ARG_WITH(includes_openssl, AS_HELP_STRING(), , includes_openssl="-I\$(with_openssl_install_dir)/include")
else
  AC_PATH_TOOL(PKGCONFIG, pkg-config)
  AS_IF([test "x$PKGCONFIG" = "x"], [AC_MSG_ERROR(pkg-config not found.)], )
  includes_openssl="`pkg-config --variable=includedir libcrypto`"
  if test "`grep "define OPENSSL_VERSION_MAJOR" $includes_openssl/openssl/opensslv.h | awk '{print $4}'`" = "3"
  then
    AC_MSG_NOTICE([Build QAT engine against OpenSSL 3.0.0])
    AC_ARG_WITH(cflags_openssl_300, AS_HELP_STRING(), , cflags_openssl_300="-DSSL_QAT_USE_ASYNC_CALLBACK")
    AC_SUBST(cflags_openssl_300)
  else
    if test "`grep "define OPENSSL_VERSION_NUMBER  0x10100" $includes_openssl/openssl/opensslv.h | wc -l`" = "1"
    then
      AC_MSG_ERROR([OpenSSL version in the system is less than 1.1.1. Either update system OpenSSL to 1.1.1 or Use "--with-openssl_install_dir" pointing to the path where OpenSSL downloaded from source is installed. Additional flag "--with-openssl_dir" pointing to the OpenSSL source dir needs to be configured for OpenSSL 1.1.0])
    fi
  fi
  engine_install_dir="`pkg-config --variable=enginesdir libcrypto`"
  AC_ARG_WITH(includes_openssl, AS_HELP_STRING(), , includes_openssl="-I`pkg-config --variable=includedir libcrypto`")
  AC_MSG_NOTICE([Install engine in the system OpenSSL enginesdir Path])
fi
AM_CONDITIONAL([QAT_OPENSSL_110], [test "x$cflags_openssl_110" != "x"])
AC_SUBST(includes_openssl)
AC_SUBST(engine_install_dir)

# If both QAT and Multibuff configured, then check the libraries from standard location and use accordingly.
if test "x$cflags_qat_intree" = "x"
then
  if test "x$with_qat_dir" != "x" -a "x$enable_multibuff_offload" = "xyes"
  then
    AC_CHECK_LIB(qat_s, cpaCyRsaDecrypt, [AC_MSG_NOTICE([QAT libraries found in the system])], [AC_MSG_NOTICE([QAT Library not found in the standard location])], [])
    # Check if QAT is installed, otherwise use Multibuff
    if test "x$ac_cv_lib_qat_s_cpaCyRsaDecrypt" = "xno"
    then
      AC_CHECK_LIB(crypto_mb, mbx_getversion, [AC_ARG_WITH(cflags_multibuff_offload, AS_HELP_STRING(), , cflags_multibuff_offload="-DOPENSSL_MULTIBUFF_OFFLOAD")], [AC_MSG_ERROR([Both QAT and Crypto Multi-buffer library not found in the standard path. Install either QAT or Crypto Multi-buffer library])], [])
      AC_SUBST(cflags_multibuff_offload)
      AM_CONDITIONAL([OPENSSL_MULTIBUFF_OFFLOAD], [test "x$ac_cv_lib_crypto_mb_mbx_getversion" = "xyes"])
    fi
  fi
fi

# qat_dir configured, enable qat offload
if test "x$with_qat_dir" != "x"
then
  if test "x$enable_qat_offload" != "xno"
  then
    AC_ARG_WITH(cflags_qat_offload, AS_HELP_STRING(), , cflags_qat_offload="-DOPENSSL_QAT_OFFLOAD")
    AC_SUBST(cflags_qat_offload)
    if test "x$with_qat_install_dir" = "x"
    then
      with_qat_install_dir="\$(with_qat_dir)/build"
    fi
    AC_MSG_NOTICE([Enabling build for QAT Offload])
  else
    AC_MSG_NOTICE([Disabling build for QAT Offload])
  fi
fi
AM_CONDITIONAL([OPENSSL_QAT_OFFLOAD], [test "x$cflags_qat_offload" != "x"])

# Multibuff offload enabled
if test "x$enable_multibuff_offload" = "xyes"
then
  if test "x$cflags_qat_offload" = "x"
  then
    AC_ARG_WITH(cflags_multibuff_offload, AS_HELP_STRING(), , cflags_multibuff_offload="-DOPENSSL_MULTIBUFF_OFFLOAD")
    AC_SUBST(cflags_multibuff_offload)
    AC_MSG_NOTICE([Enabling build for Multibuff Offload])
  fi
fi
AM_CONDITIONAL([OPENSSL_MULTIBUFF_OFFLOAD], [test "x$cflags_multibuff_offload" != "x"])

# IPSec Offload enabled
if test "x$enable_ipsec_offload" = "xyes"
then
   AC_ARG_WITH(cflags_ipsec_offload, AS_HELP_STRING(), , cflags_ipsec_offload="-DOPENSSL_IPSEC_OFFLOAD")
   AC_SUBST(cflags_ipsec_offload)
   AC_MSG_NOTICE([Enabling build for Intel IPSec Offload])
fi
AM_CONDITIONAL([OPENSSL_IPSEC_OFFLOAD], [test "x$enable_ipsec_offload" = "xyes"])

# OpenSSL source dir to regenerate err file for OpenSSL 1.1.0
if test "x$with_openssl_dir" = "x"
then
  AC_MSG_NOTICE([Build with existing error files without regenerating from OpenSSL source])
else if test "x$with_openssl_dir" = "xno"
then
  AC_MSG_ERROR([--without-openssl_dir is invalid, set using --with-openssl_dir to the path to the OpenSSL source code. e.g: --with-openssl_dir=/path/to/openssl])
fi
fi
AM_CONDITIONAL([QAT_ERR_FILES_BUILD], [test "x$with_openssl_dir" != "x"])

# Checking the parameters given and parsing the relevant flags
if test "x$enable_qat_rsa" != "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_rsa="-DOPENSSL_ENABLE_QAT_RSA"
  AC_MSG_NOTICE([Offloading RSA to Hardware])
else
  enable_qat_rsa="-DOPENSSL_DISABLE_QAT_RSA"
  AC_MSG_NOTICE([Not Offloading RSA to Hardware])
fi

if test "x$enable_qat_ciphers" != "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_ciphers="-DOPENSSL_ENABLE_QAT_CIPHERS"
  AC_MSG_NOTICE([Offloading CIPHERS to Hardware])
else
  enable_qat_ciphers="-DOPENSSL_DISABLE_QAT_CIPHERS"
  AC_MSG_NOTICE([Not Offloading CIPHERS to Hardware])
fi

if test "x$enable_qat_ecdh" != "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_ecdh="-DOPENSSL_ENABLE_QAT_ECDH"
  AC_MSG_NOTICE([Offloading ECDH to Hardware])
else
  enable_qat_ecdh="-DOPENSSL_DISABLE_QAT_ECDH"
  AC_MSG_NOTICE([Not Offloading ECDH to Hardware])
fi

if test "x$enable_qat_ecdsa" != "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_ecdsa="-DOPENSSL_ENABLE_QAT_ECDSA"
  AC_MSG_NOTICE([Offloading ECDSA to Hardware])
else
  enable_qat_ecdsa="-DOPENSSL_DISABLE_QAT_ECDSA"
  AC_MSG_NOTICE([Not Offloading ECDSA to Hardware])
fi

if test "x$enable_qat_dsa" != "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_dsa="-DOPENSSL_ENABLE_QAT_DSA"
  AC_MSG_NOTICE([Offloading DSA to Hardware])
else
  enable_qat_dsa="-DOPENSSL_DISABLE_QAT_DSA"
  AC_MSG_NOTICE([Not Offloading DSA to Hardware])
fi

if test "x$enable_qat_dh" != "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_dh="-DOPENSSL_ENABLE_QAT_DH"
  AC_MSG_NOTICE([Offloading DH to Hardware])
else
  enable_qat_dh="-DOPENSSL_DISABLE_QAT_DH"
  AC_MSG_NOTICE([Not Offloading DH to Hardware])
fi

if test "x$enable_qat_prf" != "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_prf="-DOPENSSL_ENABLE_QAT_PRF"
  AC_MSG_NOTICE([Offloading PRF to Hardware])
else
  enable_qat_prf="-DOPENSSL_DISABLE_QAT_PRF"
  AC_MSG_NOTICE([Not Offloading PRF to Hardware])
fi

if test "x$enable_qat_hkdf" = "xyes" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_hkdf="-DOPENSSL_ENABLE_QAT_HKDF"
  AC_MSG_NOTICE([Offloading HKDF to Hardware])
else
  enable_qat_hkdf="-DOPENSSL_DISABLE_QAT_HKDF"
  AC_MSG_NOTICE([Not Offloading HKDF to Hardware])
fi

if test "x$enable_qat_ecx" != "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_ecx="-DOPENSSL_ENABLE_QAT_ECX"
  AC_MSG_NOTICE([Offloading X25519/X448 to Hardware])
else
  enable_qat_ecx="-DOPENSSL_DISABLE_QAT_ECX"
  AC_MSG_NOTICE([Not Offloading X25519/X448 to Hardware])
fi

if test "x$enable_vaes_gcm" != "xno" -a "x$cflags_ipsec_offload" != "x"
then
  enable_vaes_gcm="-DOPENSSL_ENABLE_VAES_GCM"
  AC_MSG_NOTICE([Offloading AES-GCM using Intel IPSec library])
else
  enable_vaes_gcm="-DOPENSSL_DISABLE_VAES_GCM"
  AC_MSG_NOTICE([Not Offloading AES-GCM using Intel IPSec libary])
fi

if test "x$enable_multibuff_rsa" != "xno" -a "x$cflags_multibuff_offload" != "x"
then
  enable_multibuff_rsa="-DOPENSSL_ENABLE_MULTIBUFF_RSA"
  AC_MSG_NOTICE([Offloading RSA using Multi-buffer])
else
  enable_multibuff_rsa="-DOPENSSL_DISABLE_MULTIBUFF_RSA"
  AC_MSG_NOTICE([Not Offloading RSA using Multi-buffer])
fi

if test "x$enable_multibuff_ecx" != "xno" -a "x$cflags_multibuff_offload" != "x"
then
    enable_multibuff_ecx="-DOPENSSL_ENABLE_MULTIBUFF_ECX"
    AC_MSG_NOTICE([Offloading X25519 using Multi-buffer])
else
    enable_multibuff_ecx="-DOPENSSL_DISABLE_MULTIBUFF_ECX"
    AC_MSG_NOTICE([Not Offloading X25519 using Multi-buffer])
fi

if test "x$enable_qat_small_pkt_offload" = "xyes" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_small_pkt_offload="-DOPENSSL_ENABLE_QAT_SMALL_PACKET_CIPHER_OFFLOADS"
  AC_MSG_NOTICE([Offloading small packet CIPHERS to Hardware])
else
  enable_qat_small_pkt_offload=""
  AC_MSG_NOTICE([Not Offloading small packet CIPHERS to Hardware])
fi

if test "x$enable_qat_lenstra_protection" = "xno" -a "x$cflags_qat_offload" != "x"
then
  enable_qat_lenstra_protection="-DOPENSSL_DISABLE_QAT_LENSTRA_PROTECTION"
  AC_MSG_NOTICE([Lenstra attack protection disabled.])
else
  enable_qat_lenstra_protection=""
  AC_MSG_NOTICE([Lenstra attack protection enabled (default).])
fi

if test "x$enable_qat_debug" = "xyes"
then
  enable_qat_debug="-DQAT_DEBUG"
  AC_MSG_NOTICE([Enabling Engine Debug Messages])
else
  enable_qat_debug=""
  AC_MSG_NOTICE([Disabling Engine Debug Messages])
fi

if test "x$enable_qat_warnings" = "xyes"
then
  enable_qat_warnings="-DQAT_WARN"
  AC_MSG_NOTICE([Enabling Engine Warning Messages])
else
  enable_qat_warnings=""
  AC_MSG_NOTICE([Disabling Engine Warning Messages])
fi

if test "x$enable_qat_mem_debug" = "xyes"
then
  enable_qat_mem_debug="-DQAT_MEM_DEBUG"
  AC_MSG_NOTICE([Enabling Memory Driver Debug Messages])
else
  enable_qat_mem_debug=""
  AC_MSG_NOTICE([Disabling Memory Driver Debug Messages])
fi

if test "x$enable_qat_mem_warnings" = "xyes"
then
  enable_qat_mem_warnings="-DQAT_MEM_WARN"
  AC_MSG_NOTICE([Enabling Memory Driver Warning Messages])
else
  enable_qat_mem_warnings=""
  AC_MSG_NOTICE([Disabling Memory Driver Warning Messages])
fi

if test "x$enable_qat_auto_engine_init_on_fork" = "xno"
then
  enable_qat_auto_engine_init_on_fork="-DOPENSSL_DISABLE_QAT_AUTO_ENGINE_INIT_ON_FORK"
  AC_MSG_NOTICE([Auto engine init on fork disabled.])
else
  enable_qat_auto_engine_init_on_fork=""
  AC_MSG_NOTICE([Auto Engine init on fork enabled (default).])
fi

if test "x$enable_multibuff_heuristic_timeout" = "xyes" -a "x$cflags_multibuff_offload" != "x"
then
  enable_multibuff_heuristic_timeout="-DMULTIBUFF_HEURISTIC_TIMEOUT"
  AC_MSG_NOTICE([Enabling Multi-buffer Heuristic Timeout])
else
  enable_multibuff_heuristic_timeout=""
  AC_MSG_NOTICE([Disabling Multi-buffer Heuristic Timeout (default)])
fi

if test "x$enable_qat_cycle_counts" = "xyes"
then
  enable_qat_cycle_counts="-DQAT_CPU_CYCLES_COUNT"
  AC_MSG_NOTICE([Enabling CPU Cycle Counts])
else
  enable_qat_cycle_counts=""
  AC_MSG_NOTICE([Disabling CPU Cycle Counts])
fi

# Compiler security flags
case "$host_os" in
*linux*)
  if test "`cc --version | head -1 | awk '{print $3>=4.9}' 2>/dev/null`" = "1"
  then
    AC_ARG_WITH(cflags, AS_HELP_STRING(), , cflags="-shared -fPIC -Wall -Wformat -Wformat-security -O2 -D_FORTIFY_SOURCE=2 -fno-delete-null-pointer-checks -fwrapv -fstack-protector-strong -fno-strict-overflow")
  else
    AC_ARG_WITH(cflags, AS_HELP_STRING(), , cflags="-shared -fPIC -Wall -Wformat -Wformat-security -O2 -D_FORTIFY_SOURCE=2 -fno-delete-null-pointer-checks -fwrapv -fstack-protector -fno-strict-overflow")
  fi
;;
*freebsd*)
    AC_ARG_WITH(cflags, AS_HELP_STRING(), , cflags="-shared -fPIC -Wall -Wformat -Wformat-security -O2 -D_FORTIFY_SOURCE=2 -fno-delete-null-pointer-checks -fwrapv -fstack-protector-strong")
;;
*) ;;
esac
AC_SUBST(cflags)

if test "x$with_cc_opt" != "x"
then
  AC_ARG_WITH(cflags_cc_opt, AS_HELP_STRING(), , cflags_cc_opt="\$(with_cc_opt)")
  AC_SUBST(cflags_cc_opt)
fi

if test "x$cflags_qat_offload" != "x"
then
  if test "x$enable_qat_contig_mem" = "xyes" -a "x$enable_multi_thread" != "xyes"
  then
    AC_MSG_NOTICE([Compiling for qat_contig_mem])
    AC_ARG_WITH(cflags_mem_driver, AS_HELP_STRING(), , cflags_mem_driver="-DUSE_QAT_CONTIG_MEM -Iqat_contig_mem")
  else if test "x$enable_multi_thread" = "xyes"
  then
    AC_MSG_NOTICE([Compiling for multi_thread])
    AC_ARG_WITH(cflags_mem_driver, AS_HELP_STRING(), , cflags_mem_driver="-DUSE_QAT_CONTIG_MEM -Iqat_contig_mem")
  else
    AC_MSG_NOTICE([Compiling for USDM])
    AC_ARG_WITH(cflags_mem_driver, AS_HELP_STRING(), , cflags_mem_driver="-DUSE_QAE_MEM")
  fi
  fi
AC_SUBST(cflags_mem_driver)
fi
AM_CONDITIONAL([QAT_CONTIG_MEM], [test "x$enable_qat_contig_mem" = "xyes" -a "x$enable_multi_thread" != "xyes"])
AM_CONDITIONAL([QAT_MULTI_THREAD], [test "x$enable_multi_thread" = "xyes"])
AM_CONDITIONAL([QAE_MEM], [test "x$enable_qat_contig_mem" != "xyes" -a "x$enable_multi_thread" != "xyes"])

if test "x$with_qat_debug_file" != "x"
then
  AC_ARG_WITH(cflags_qat_debug_file, AS_HELP_STRING(), , cflags_qat_debug_file="-DQAT_DEBUG_FILE_PATH=\$(with_qat_debug_file)")
  AC_SUBST(cflags_qat_debug_file)
  AC_MSG_NOTICE([Enabling writing debug to file])
fi

if test "x$with_qat_engine_id" != "x"
then
  AC_ARG_WITH(cflags_qat_engine_id, AS_HELP_STRING(), , cflags_qat_engine_id="-DQAT_ENGINE_ID=\$(with_qat_engine_id)")
  AC_SUBST(cflags_qat_engine_id)
  AC_MSG_NOTICE([Using engine id other than default])
else
  AC_SUBST(with_qat_engine_id, qatengine)
  AC_MSG_NOTICE([Using default engine id "qatengine"])
fi

case "$host_os" in
linux*)
  AC_CHECK_PROG(USE_LDD, ldd, yes, no)
  AC_CHECK_PROG(USE_HEAD, head, yes, no)
  if test $USE_LDD == "yes" -a $USE_HEAD
  then
    if test "`ldd --version | head -1 | awk '{print $4>=2.23?"1":"0"}' 2>/dev/null`" = "1"
    then
      AC_MSG_NOTICE([glibc version >= 2.23. glibc AVX-512 optimisation supported.])
    else
      AC_MSG_NOTICE([glibc version < 2.23. glibc AVX-512 optimisation not supported.])
    fi
    if test "`ldd --version | head -1 | awk '{print $4<2.17?"1":"0"}' 2>/dev/null`" = "1"
    then
      AC_ARG_WITH(LIBS, AS_HELP_STRING(), , LIBS+="-lrt")
      AC_SUBST(LIBS)
    fi
  else
    AC_MSG_NOTICE([glibc version could not be auto detected. Check manually using 'ldd --version'])
    AC_MSG_NOTICE([glibc AVX-512 optimisation supported only from glibc version 2.23])
    AC_ARG_WITH(LIBS, AS_HELP_STRING(), , LIBS+="-lrt")
    AC_SUBST(LIBS)

  fi
  ;;
  *)
esac

# Setting driver headers include path
if test "x$cflags_qat_offload" != "x"
then
  if test "x$cflags_qat_intree" != "x"
  then
    AC_ARG_WITH(includes_driver, AS_HELP_STRING(), , includes_driver="-I/usr/include/qat")
    AC_SUBST(includes_driver)
  else
    AC_ARG_WITH(ICP_API_DIR, AS_HELP_STRING(), ,with_ICP_API_DIR="\$(with_qat_dir)/quickassist/include")
    AC_SUBST(with_ICP_API_DIR)

    AC_ARG_WITH(ICP_SAL_API_DIR, AS_HELP_STRING(), ,with_ICP_SAL_API_DIR="\$(with_qat_dir)/quickassist/lookaside/access_layer/include")
    AC_SUBST(with_ICP_SAL_API_DIR)

    AC_ARG_WITH(ICP_LAC_API_DIR, AS_HELP_STRING(), ,with_ICP_LAC_API_DIR="\$(with_ICP_API_DIR)/lac")
    AC_SUBST(with_ICP_LAC_API_DIR)

    AC_ARG_WITH(includes_driver, AS_HELP_STRING(), , includes_driver="-I\$(with_ICP_API_DIR) -I\$(with_ICP_LAC_API_DIR) -I\$(with_ICP_SAL_API_DIR)")
    AC_SUBST(includes_driver)
  fi
fi

if test "x$cflags_qat_intree" != "x"
then
  AC_ARG_WITH(DRIVER, AS_HELP_STRING(), , DRIVER="qat")
  AC_ARG_WITH(USDM, AS_HELP_STRING(), , USDM="usdm")
else
  AC_ARG_WITH(DRIVER, AS_HELP_STRING(), , DRIVER="qat_s")
  AC_ARG_WITH(USDM, AS_HELP_STRING(), , USDM="usdm_drv_s")
fi
AC_SUBST(DRIVER)
AC_SUBST(USDM)

if test "x$with_ld_opt" != "x"
then
  AC_ARG_WITH(QAT_SHARED_LIB_DEPS_LD, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_LD=["\$(with_ld_opt)"])
  AC_SUBST(QAT_SHARED_LIB_DEPS_LD)
fi

# Setting QAT, crypto_mb and IPSec install dir for library and headers
if test "x$cflags_qat_offload" != "x"
then
  if test "x$with_qat_install_dir" != "x"
  then
    AC_ARG_WITH(QAT_SHARED_LIB_DEPS_DRIVER, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_DRIVER=["-Wl,-rpath,\$(with_qat_install_dir) -L\$(with_qat_install_dir) -l\$(DRIVER)"])
  else
    AC_ARG_WITH(QAT_SHARED_LIB_DEPS_DRIVER, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_DRIVER=["-l\$(DRIVER)"])
  fi
AC_SUBST(QAT_SHARED_LIB_DEPS_DRIVER)
fi

if test "x$cflags_multibuff_offload" != "x"
then
  if test "x$with_multibuff_install_dir" != "x"
  then
    AC_MSG_NOTICE([Using crypto_mb library from the path provided in multibuff_install_dir])
    AC_ARG_WITH(includes_multibuff, AS_HELP_STRING(), , includes_multibuff="-I\$(with_multibuff_install_dir)/include")
    AC_ARG_WITH(QAT_SHARED_LIB_DEPS_MULTIBUFF, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_MULTIBUFF=["-Wl,-rpath,\$(with_multibuff_install_dir)/lib -L\$(with_multibuff_install_dir)/lib -lcrypto_mb"])
  else
    AC_CHECK_LIB(crypto_mb, mbx_getversion, [AC_MSG_NOTICE([Using crypto_mb Library from default location])], [AC_MSG_ERROR([crypto_mb Library not found, Install the crypto_mb library or provide the path to the library using --with-multibuff_install_dir])],[])
    AC_ARG_WITH(includes_multibuff, AS_HELP_STRING(), , includes_multibuff="-I/usr/local/include -I/usr/include")
    AC_ARG_WITH(QAT_SHARED_LIB_DEPS_MULTIBUFF, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_MULTIBUFF=["-lcrypto_mb"])
  fi
AC_SUBST(includes_multibuff)
AC_SUBST(QAT_SHARED_LIB_DEPS_MULTIBUFF)
fi

if test "x$cflags_ipsec_offload" != "x"
then
  if test "x$with_ipsec_install_dir" != "x"
  then
    AC_ARG_WITH(includes_ipsec, AS_HELP_STRING(), , includes_ipsec="-I\$(with_ipsec_install_dir)/include")
    AC_ARG_WITH(QAT_SHARED_LIB_DEPS_IPSEC, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_IPSEC=["-Wl,-rpath,\$(with_ipsec_install_dir)/lib -L\$(with_ipsec_install_dir)/lib -lIPSec_MB"])
  else
    AC_MSG_NOTICE([Using Intel IPsec library from default location])
    AC_ARG_WITH(includes_ipsec, AS_HELP_STRING(), , includes_ipsec="-I/usr/include")
    AC_ARG_WITH(QAT_SHARED_LIB_DEPS_IPSEC, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_IPSEC=["-lIPSec_MB"])
  fi
AC_SUBST(includes_ipsec)
AC_SUBST(QAT_SHARED_LIB_DEPS_IPSEC)
fi

if test "x$cflags_qat_offload" != "x"
then
  if test "x$enable_qat_contig_mem" != "xyes" -a "x$enable_multi_thread" != "xyes"
  then
    if test "x$with_usdm_dir" = "x" -a "x$cflags_qat_intree" = "x"
    then
      with_usdm_dir="\$(with_qat_dir)/quickassist/utilities/libusdm_drv"
      AC_ARG_WITH(QAT_SHARED_LIB_DEPS_QAE_MEM, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_QAE_MEM=["-Wl,-rpath,\$(with_usdm_dir) -L\$(with_usdm_dir) -l\$(USDM)"])
      AC_ARG_WITH(includes_usdm, AS_HELP_STRING(), , includes_usdm="-I\$(with_usdm_dir)")
      AC_SUBST(includes_usdm)
    else
      AC_ARG_WITH(QAT_SHARED_LIB_DEPS_QAE_MEM, AS_HELP_STRING(), , QAT_SHARED_LIB_DEPS_QAE_MEM=["-l\$(USDM)"])
    fi
  fi
AC_SUBST(QAT_SHARED_LIB_DEPS_QAE_MEM)
fi

# Output files from the configure
AC_CONFIG_FILES([Makefile])
AC_OUTPUT
