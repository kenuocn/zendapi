set(ZAPI_PUBLIC_HEADERS
   ${ZAPI_INCLUDE_DIR}/apidoc.h
   ${ZAPI_INCLUDE_DIR}/zapi/CompilerDetection.h
   ${ZAPI_INCLUDE_DIR}/zapi/Global.h
   ${ZAPI_INCLUDE_DIR}/zapi/PhpHeaders.h
   ${ZAPI_INCLUDE_DIR}/zapi/Typedefs.h
   ${ZAPI_INCLUDE_DIR}/zapi/ProcessorDetection.h 
   ${ZAPI_INCLUDE_DIR}/zapi/SystemDetection.h
   ${ZAPI_INCLUDE_DIR}/zapi/ZendApi.h
   ${ZAPI_INCLUDE_DIR}/zapi/stdext/Functional.h
   ${ZAPI_INCLUDE_DIR}/zapi/stdext/TypeTraits.h
   ${ZAPI_INCLUDE_DIR}/zapi/stdext/Tuple.h
   ${ZAPI_INCLUDE_DIR}/zapi/stdext/internal/FunctionalPrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/stdext/internal/TuplePrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/protocol/AbstractIterator.h
   ${ZAPI_INCLUDE_DIR}/zapi/protocol/ArrayAccess.h
   ${ZAPI_INCLUDE_DIR}/zapi/protocol/Countable.h
   ${ZAPI_INCLUDE_DIR}/zapi/protocol/Serializable.h
   ${ZAPI_INCLUDE_DIR}/zapi/protocol/Traversable.h
   ${ZAPI_INCLUDE_DIR}/zapi/kernel/Meta.h
   ${ZAPI_INCLUDE_DIR}/zapi/kernel/StreamBuffer.h
   ${ZAPI_INCLUDE_DIR}/zapi/kernel/NotImplemented.h
   ${ZAPI_INCLUDE_DIR}/zapi/kernel/OrigException.h
   ${ZAPI_INCLUDE_DIR}/zapi/kernel/FatalError.h
   ${ZAPI_INCLUDE_DIR}/zapi/kernel/Exception.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Extension.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Ini.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/internal/ExtensionPrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Type.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Class.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Interface.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Constant.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/internal/NamespacePrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/StdClass.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Parameters.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Namespace.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Argument.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Function.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/Method.h
   ${ZAPI_INCLUDE_DIR}/zapi/lang/internal/StdClassPrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/Variant.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/StringVariant.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/BoolVariant.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/NumericVariant.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/DoubleVariant.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/ObjectVariant.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/CallableVariant.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/ArrayVariant.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/ArrayItemProxy.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/internal/VariantPrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/ds/internal/ArrayItemProxyPrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/utils/PhpFuncs.h
   ${ZAPI_INCLUDE_DIR}/zapi/utils/CommonFuncs.h
   ${ZAPI_INCLUDE_DIR}/zapi/utils/InternalFuncs.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/AbstractClass.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/InvokeBridge.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/Callable.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/internal/CallablePrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/internal/AbstractClassPrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/internal/AbstractMemberPrivate.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/Engine.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/AbstractMember.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/ZValMember.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/StringMember.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/BoolMember.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/FloatMember.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/NumericMember.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/NullMember.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/Property.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/ExecStateGuard.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/IteratorBridge.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/ObjectBinder.h
   ${ZAPI_INCLUDE_DIR}/zapi/vm/Closure.h
   )

set(ZAPI_PUBLIC_HEADERS ${ZAPI_PUBLIC_HEADERS} PARENT_SCOPE)
set(ZAPI_PRIVATE_HEADERS ${ZAPI_PRIVATE_HEADERS} PARENT_SCOPE)

# install header files
install(DIRECTORY ${ZAPI_INCLUDE_DIR}/zapi
   DESTINATION
   "${ZAPI_INSTALL_INCLUDE_DIR}"
   COMPONENT dev
   FILES_MATCHING PATTERN "*.h")

# install generate header files
install(DIRECTORY ${ZAPI_EXTRA_INCLUDE_DIR}/zapi
   DESTINATION
   "${ZAPI_INSTALL_INCLUDE_DIR}"
   COMPONENT dev
   FILES_MATCHING PATTERN "*.h")

