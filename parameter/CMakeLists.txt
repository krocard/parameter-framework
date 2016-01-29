# Copyright (c) 2014-2015, Intel Corporation
# All rights reserved.
#
# Redistribution and use in source and binary forms, with or without modification,
# are permitted provided that the following conditions are met:
#
# 1. Redistributions of source code must retain the above copyright notice, this
# list of conditions and the following disclaimer.
#
# 2. Redistributions in binary form must reproduce the above copyright notice,
# this list of conditions and the following disclaimer in the documentation and/or
# other materials provided with the distribution.
#
# 3. Neither the name of the copyright holder nor the names of its contributors
# may be used to endorse or promote products derived from this software without
# specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
# ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
# WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
# DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR
# ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
# (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
# LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON
# ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
# (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
# SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

if(WIN32)
    set(parameter_RESOURCE_FILE "${CMAKE_CURRENT_BINARY_DIR}/Resource.rc")
    set(parameter_OS_SPECIFIC_SRCS ${parameter_RESOURCE_FILE})
endif()

add_library(parameter SHARED
    ${parameter_OS_SPECIFIC_SRCS}
    AreaConfiguration.cpp
    AreaConfiguration.h
    ArrayParameter.cpp
    ArrayParameter.h
    BackSynchronizer.h
    BaseParameter.cpp
    BaseParameter.h
    BitParameter.cpp
    BitParameter.h
    BitParameterBlock.cpp
    BitParameterBlock.h
    BitParameterBlockType.cpp
    BitParameterBlockType.h
    BitParameterType.cpp
    BitParameterType.h
    BitwiseAreaConfiguration.cpp
    BitwiseAreaConfiguration.h
    BooleanParameterType.cpp
    BooleanParameterType.h
    CommandHandlerWrapper.cpp
    CommandHandlerWrapper.h
    Component.h
    ComponentInstance.cpp
    ComponentInstance.h
    ComponentLibrary.cpp
    ComponentLibrary.h
    ComponentType.cpp
    ComponentType.h
    CompoundRule.cpp
    CompoundRule.h
    ConfigurableDomain.cpp
    ConfigurableDomain.h
    ConfigurableDomains.cpp
    ConfigurableDomains.h
    ConfigurableElement.cpp
    ConfigurableElement.h
    ConfigurableElementAggregator.cpp
    ConfigurableElementAggregator.h
    ConfigurationAccessContext.cpp
    ConfigurationAccessContext.h
    DefaultElementLibrary.h
    DomainConfiguration.cpp
    DomainConfiguration.h
    Element.cpp
    Element.h
    ElementBuilder.h
    ElementBuilderTemplate.h
    ElementHandle.cpp
    ElementLibrary.cpp
    ElementLibrary.h
    ElementLibrarySet.cpp
    ElementLibrarySet.h
    ElementLocator.cpp
    ElementLocator.h
    EnumParameterType.cpp
    EnumParameterType.h
    EnumValuePair.cpp
    EnumValuePair.h
    FileIncluderElementBuilder.h
    FixedPointParameterType.cpp
    FixedPointParameterType.h
    FloatingPointParameterType.cpp
    FloatingPointParameterType.h
    FormattedSubsystemObject.cpp
    FormattedSubsystemObject.h
    FrameworkConfigurationGroup.h
    FrameworkConfigurationLocation.cpp
    FrameworkConfigurationLocation.h
    HardwareBackSynchronizer.cpp
    HardwareBackSynchronizer.h
    InstanceConfigurableElement.cpp
    InstanceConfigurableElement.h
    InstanceDefinition.cpp
    InstanceDefinition.h
    IntegerParameterType.cpp
    IntegerParameterType.h
    KindElement.h
    KindElementBuilderTemplate.h
    LinearParameterAdaptation.cpp
    LinearParameterAdaptation.h
    LogarithmicParameterAdaptation.cpp
    LogarithmicParameterAdaptation.h
    LoggingElementBuilderTemplate.cpp
    LoggingElementBuilderTemplate.h
    Mapper.h
    MappingContext.cpp
    MappingContext.h
    MappingData.cpp
    MappingData.h
    NamedElementBuilderTemplate.h
    Parameter.cpp
    Parameter.h
    ParameterAccessContext.cpp
    ParameterAccessContext.h
    ParameterAdaptation.cpp
    ParameterAdaptation.h
    ParameterBlackboard.cpp
    ParameterBlackboard.h
    ParameterBlock.h
    ParameterBlockType.cpp
    ParameterBlockType.h
    ParameterFrameworkConfiguration.cpp
    ParameterFrameworkConfiguration.h
    ParameterMgr.cpp
    ParameterMgr.h
    ParameterMgrFullConnector.cpp
    ParameterMgrLogger.h
    ParameterMgrPlatformConnector.cpp
    ParameterType.cpp
    ParameterType.h
    PathNavigator.cpp
    PathNavigator.h
    Plugin.h
    PluginLocation.cpp
    PluginLocation.h
    Results.h
    Rule.h
    RuleParser.cpp
    RuleParser.h
    SelectionCriteria.cpp
    SelectionCriteria.h
    SelectionCriteriaDefinition.cpp
    SelectionCriteriaDefinition.h
    SelectionCriterion.cpp
    SelectionCriterion.h
    SelectionCriterionLibrary.cpp
    SelectionCriterionLibrary.h
    SelectionCriterionRule.cpp
    SelectionCriterionRule.h
    SelectionCriterionType.cpp
    SelectionCriterionType.h
    SimulatedBackSynchronizer.cpp
    SimulatedBackSynchronizer.h
    StringParameter.cpp
    StringParameter.h
    StringParameterType.cpp
    StringParameterType.h
    Subsystem.cpp
    Subsystem.h
    SubsystemElementBuilder.cpp
    SubsystemElementBuilder.h
    SubsystemLibrary.h
    SubsystemObject.cpp
    SubsystemObject.h
    SubsystemObjectCreator.cpp
    SubsystemObjectCreator.h
    SubsystemObjectFactory.h
    SubsystemPlugins.h
    Syncer.h
    SyncerSet.cpp
    SyncerSet.h
    SystemClass.cpp
    SystemClass.h
    TypeElement.cpp
    TypeElement.h
    VirtualSubsystem.cpp
    VirtualSubsystem.h
    VirtualSyncer.cpp
    VirtualSyncer.h
    XmlDomainExportContext.h
    XmlDomainImportContext.h
    XmlDomainSerializingContext.h
    XmlElementSerializingContext.cpp
    XmlElementSerializingContext.h
    XmlFileIncluderElement.cpp
    XmlFileIncluderElement.h
    XmlParameterSerializingContext.cpp
    XmlParameterSerializingContext.h
    include/CommandHandlerInterface.h
    include/ElementHandle.h
    include/ParameterHandle.h
    include/ParameterMgrFullConnector.h
    include/ParameterMgrLoggerForward.h
    include/ParameterMgrPlatformConnector.h
    include/SelectionCriterionInterface.h
    include/SelectionCriterionTypeInterface.h
    log/include/log/Context.h
    log/include/log/ILogger.h
    log/include/log/LogWrapper.h
    log/include/log/Logger.h
)

include(GenerateExportHeader)
generate_export_header(parameter)

if(WIN32)
    set(WINRC_MAJOR ${PF_VERSION_MAJOR})
    set(WINRC_MINOR ${PF_VERSION_MINOR})
    set(WINRC_PATCH ${PF_VERSION_PATCH})
    set(WINRC_TWEAK ${PF_VERSION_TWEAK})
    target_compile_definitions(parameter PRIVATE
        WINRC_DLL
        WINRC_FILENAME="$<TARGET_FILE_NAME:parameter>")
    set(WINRC_FILE_DESCRIPTION "Parameter Framework library")
    configure_file("${PROJECT_SOURCE_DIR}/support/windows/Resource.rc.in"
                   "${parameter_RESOURCE_FILE}")
endif()

configure_file(version.h.in "${CMAKE_CURRENT_BINARY_DIR}/version.h")

target_link_libraries(parameter
    # Unfortunatly xmlSink and xmlSource need to be exposed to the plugins
    PUBLIC xmlserializer
    PRIVATE pfw_utility remote-processor
    PRIVATE ${CMAKE_DL_LIBS})

target_include_directories(parameter
    PUBLIC include log/include
    # Export symbol macro header
    PUBLIC "${CMAKE_CURRENT_BINARY_DIR}"
    # FIXE: define . as an PUBLIC include directory only for plugins
    PUBLIC .)

install(TARGETS parameter LIBRARY DESTINATION lib RUNTIME DESTINATION bin ARCHIVE DESTINATION lib)
# Client headers
install(FILES
    "${CMAKE_CURRENT_BINARY_DIR}/parameter_export.h"
    include/CommandHandlerInterface.h
    include/ElementHandle.h
    include/ParameterHandle.h
    include/ParameterMgrLoggerForward.h
    include/ParameterMgrFullConnector.h
    include/ParameterMgrPlatformConnector.h
    include/SelectionCriterionInterface.h
    include/SelectionCriterionTypeInterface.h
    DESTINATION "include/parameter/client")
# Core (plugin) headers
install(FILES
    "${CMAKE_CURRENT_BINARY_DIR}/parameter_export.h"
    BitParameterBlockType.h
    ConfigurableElement.h
    DefaultElementLibrary.h
    Element.h
    ElementBuilder.h
    ElementLibrary.h
    FileIncluderElementBuilder.h
    FormattedSubsystemObject.h
    InstanceConfigurableElement.h
    LoggingElementBuilderTemplate.h
    Mapper.h
    MappingContext.h
    ParameterBlockType.h
    ParameterType.h
    PathNavigator.h
    Plugin.h
    Subsystem.h
    SubsystemLibrary.h
    SubsystemObject.h
    SubsystemObjectCreator.h
    SubsystemObjectFactory.h
    Syncer.h
    TypeElement.h
    VirtualSubsystem.h
    DESTINATION "include/parameter/plugin")
install(DIRECTORY log/include/log/
        DESTINATION "include/parameter/plugin/log")
