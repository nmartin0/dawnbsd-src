# $OpenBSD: Makefile,v 1.29 2025/06/29 01:36:32 jmatthew Exp $

.include <bsd.own.mk>

.include "Makefile.arch"

# order!
SUBDIR=	include/llvm/Config
SUBDIR+=libLLVMSupport
SUBDIR+=libLLVMTableGen
SUBDIR+=llvm-min-tblgen
SUBDIR+=llvm-tblgen
SUBDIR+=include/llvm/ExecutionEngine/JITLink
SUBDIR+=include/llvm/IR
SUBDIR+=include/llvm/Frontend/OpenACC
SUBDIR+=include/llvm/Frontend/OpenMP
SUBDIR+=include/llvm/TargetParser

.for arch in ${LLVM_ARCHS}
.if "${arch}" == ${LLVM_ARCH} || "${arch}" == "AMDGPU" || make(obj)
SUBDIR+=include/llvm/${arch}
.endif
.endfor

SUBDIR+=libLLVM
SUBDIR+=llvm-config

SUBDIR+=libclangSupport

SUBDIR+=clang-tblgen
SUBDIR+=include/clang

SUBDIR+=libclangAPINotes
SUBDIR+=libclangBasic
SUBDIR+=libclangBasicTargets
SUBDIR+=libclangLex
SUBDIR+=libclangParse
SUBDIR+=libclangAST
SUBDIR+=libclangASTMatchers
SUBDIR+=libclangSema
SUBDIR+=libclangCodeGen
SUBDIR+=libclangAnalysis
SUBDIR+=libclangEdit
SUBDIR+=libclangRewrite
SUBDIR+=libclangDriver
SUBDIR+=libclangSerialization
SUBDIR+=libclangFrontend
SUBDIR+=libclangRewriteFrontend
SUBDIR+=libclangFrontendTool
SUBDIR+=libclangExtractAPI
SUBDIR+=libclangIndex
SUBDIR+=libclangInstallAPI

SUBDIR+=clang

SUBDIR+=include/lld/ELF

SUBDIR+=liblldCommon
SUBDIR+=liblldELF

SUBDIR+=lld

.if ${BUILD_LLDB:L} == "yes" || make(obj)
SUBDIR+=lldb-tblgen
SUBDIR+=include/lldb/Commands
SUBDIR+=include/lldb/Core
SUBDIR+=include/lldb/Interpreter
SUBDIR+=include/lldb/Plugins
SUBDIR+=include/lldb/Target

SUBDIR+=liblldbABI
SUBDIR+=liblldbAPI
SUBDIR+=liblldbBreakpoint
SUBDIR+=liblldbCommands
SUBDIR+=liblldbCore
SUBDIR+=liblldbDataFormatters
SUBDIR+=liblldbExpression
SUBDIR+=liblldbHostCommon
SUBDIR+=liblldbHostOpenBSD
SUBDIR+=liblldbHostPOSIX
SUBDIR+=liblldbInitialization
SUBDIR+=liblldbInterpreter
SUBDIR+=liblldbPluginArchitecture
SUBDIR+=liblldbPluginDisassembler
SUBDIR+=liblldbPluginDynamicLoader
SUBDIR+=liblldbPluginExpressionParser
SUBDIR+=liblldbPluginInstruction
SUBDIR+=liblldbPluginInstrumentationRuntime
SUBDIR+=liblldbPluginJITLoader
SUBDIR+=liblldbPluginLanguage
SUBDIR+=liblldbPluginLanguageRuntime
SUBDIR+=liblldbPluginMemoryHistory
SUBDIR+=liblldbPluginObjectContainer
SUBDIR+=liblldbPluginObjectFile
SUBDIR+=liblldbPluginPlatform
SUBDIR+=liblldbPluginProcess
SUBDIR+=liblldbPluginRegisterTypeBuilder
SUBDIR+=liblldbPluginScriptInterpreter
SUBDIR+=liblldbPluginStructuredData
SUBDIR+=liblldbPluginSymbolFile
SUBDIR+=liblldbPluginSymbolLocator
SUBDIR+=liblldbPluginSymbolVendor
SUBDIR+=liblldbPluginSystemRuntime
SUBDIR+=liblldbPluginTypeSystem
SUBDIR+=liblldbPluginUnwindAssembly
SUBDIR+=liblldbSymbol
SUBDIR+=liblldbTarget
SUBDIR+=liblldbUtility

SUBDIR+=lldb
SUBDIR+=lldb-server
.endif

SUBDIR+=libLLVMObjCopy
SUBDIR+=include/llvm-objcopy
SUBDIR+=llvm-objcopy
SUBDIR+=include/llvm-objdump
SUBDIR+=llvm-objdump
SUBDIR+=include/llvm-readobj
SUBDIR+=llvm-readobj
SUBDIR+=include/llvm-symbolizer
SUBDIR+=llvm-symbolizer

SUBDIR+=llvm-profdata
SUBDIR+=llvm-cov

.if ${AR_VERSION:L} == "llvm" || make(obj)
SUBDIR+=libLLVMDlltoolDriver
SUBDIR+=libLLVMLibDriver
SUBDIR+=llvm-ar
.endif

.include <bsd.obj.mk>
.include <bsd.subdir.mk>
