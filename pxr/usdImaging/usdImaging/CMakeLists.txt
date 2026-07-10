set(PXR_PREFIX pxr/usdImaging)
set(PXR_PACKAGE usdImaging)

pxr_library(usdImaging
    LIBRARIES
        gf
        tf
        plug
        trace
        vt
        work
        geomUtil
        hd
        hdar
        hdsi
        hio
        pxOsd
        sdf
        usd
        usdGeom
        usdLux
        usdRender
        usdShade
        usdSkel
        usdVol
        ar
        TBB::tbb

    PUBLIC_CLASSES
        adapterRegistry
        collectionCache
        collectionMaterialBindingSchema
        collectionPredicateLibrary
        directMaterialBindingSchema
        dataSourceAttribute
        dataSourceAttributeColorSpace
        dataSourceAttributeTypeName
        dataSourceBasisCurves
        dataSourceCamera
        dataSourceGprim
        dataSourceMapped
        dataSourceMaterial
        dataSourceMesh
        dataSourceNurbsCurves
        dataSourceNurbsPatch
        dataSourcePointInstancer
        dataSourcePoints
        dataSourcePrim
        dataSourcePrimvars
        dataSourceRelationship
        dataSourceRenderPrims
        dataSourceStage
        dataSourceStageGlobals
        dataSourceTetMesh
        dataSourceUsdPrimInfo
        dataSourceVolume
        debugCodes
        delegate
        drawModeAdapter
        drawModeSceneIndex
        extentResolvingSceneIndex
        extentsHintSchema
        geomModelSchema
        geomXformVectorsSchema
        geomSubsetAdapter
        indexProxy
        legacyRenderSettingsSceneIndex
        materialParamUtils
        modelSchema
        primvarUtils
        prototypeSceneIndexUtils
        resolvedAttributeCache
        instancerContext
        stageSceneIndex
        selectionSceneIndex
        tokens
        apiSchemaAdapter
        backPlateAPIAdapter
        basisCurvesAdapter
        capsuleAdapter
        cameraAdapter
        collectionAPIAdapter
        coneAdapter
        coordSysAdapter
        coordSysAPIAdapter
        cubeAdapter
        cylinderAdapter
        cylinderLightAdapter
        diskLightAdapter
        distantLightAdapter
        domeLightAdapter
        domeLight_1Adapter
        fieldAdapter
        flattenedDataSourceProviders
        flattenedGeomModelDataSourceProvider
        flattenedMaterialBindingsDataSourceProvider
        geometryLightAdapter
        geomModelAPIAdapter
        gprimAdapter
        hermiteCurvesAdapter
        implicitSurfaceMeshUtils
        instanceablePrimAdapter
        instanceAdapter
        lightAdapter
        lightAPIAdapter
        lightFilterAdapter
        materialAdapter
        materialBindingAPIAdapter
        materialBindingSchema
        materialBindingsSchema
        materialBindingsResolvingSceneIndex
        meshAdapter
        motionAPIAdapter
        niPrototypePropagatingSceneIndex
        nurbsCurvesAdapter
        nurbsPatchAdapter
        piPrototypePropagatingSceneIndex
        planeAdapter
        pluginLightAdapter
        pluginLightFilterAdapter
        pointsAdapter
        pointInstancerAdapter
        portalLightAdapter
        primAdapter
        primvarDescCache
        rootOverridesSceneIndex
        unloadedDrawModeSceneIndex
        usdPrimInfoSchema
        usdRenderProductSchema
        usdRenderSettingsSchema
        usdRenderVarSchema
        usdUpAxisSchema
        rectLightAdapter
        renderPassAdapter
        renderProductAdapter
        renderSettingsAdapter
        renderSettingsFlatteningSceneIndex
        renderVarAdapter
        representedByAncestorPrimAdapter
        rerootingContainerDataSource
        rerootingSceneIndex
        sceneIndex
        sceneIndexCreateArgsSchema
        sceneIndexPlugin
        sceneIndexPrimAdapter
        sceneIndices
        sphereAdapter
        sphereLightAdapter
        tetMeshAdapter
        textureUtils
        volumeAdapter

    PRIVATE_CLASSES
        adapterManager
        dataSourceRelocatingSceneIndex
        drawModeStandin
        instanceProxyPathTranslationSceneIndex
        niInstanceAggregationSceneIndex
        niPrototypePruningSceneIndex
        niPrototypeSceneIndex
        piPrototypeSceneIndex

    PUBLIC_HEADERS
        api.h
        types.h
        unitTestHelper.h
        version.h

    PRIVATE_HEADERS
        dataSourceImplicits-Impl.h

    RESOURCE_FILES
        plugInfo.json
)

# Build tests
pxr_build_test(testUsdImagingDataSourceAttribute
    LIBRARIES
        usdImaging
        usd
        sdf
        hd
        tf
    CPPFILES
        testenv/testUsdImagingDataSourceAttribute.cpp
)
pxr_build_test(testUsdImagingDelegate
    LIBRARIES
        usdImaging
        usdGeom
        usd
        hd
        tf
        gf
        arch
    CPPFILES
        testenv/testUsdImagingDelegate.cpp
)
pxr_build_test(testUsdImagingDelegateChanges
    LIBRARIES
        usdImaging
        usdShade
        usdGeom
        usd
        sdf
        hd
        tf
        gf
        arch
    CPPFILES
        testenv/testUsdImagingDelegateChanges.cpp
)
pxr_build_test(testUsdImagingExcluded
    LIBRARIES
        usdImaging
        usdGeom
        usd
        hd
        gf
        arch
    CPPFILES
        testenv/testUsdImagingExcluded.cpp
)
pxr_build_test(testUsdImagingMaterialBinding
    LIBRARIES
        usdImaging
        usdShade
        usd
        hd
        garch
        tf
        gf
        vt
    CPPFILES
        testenv/testUsdImagingMaterialBinding.cpp
)
pxr_build_test(testUsdImagingNestedInstancingCategories
    LIBRARIES
        usdImaging
        usd
        tf
    CPPFILES
        testenv/testUsdImagingNestedInstancingCategories.cpp
)
pxr_build_test(testUsdImagingPrimvarUtils
    LIBRARIES
        usdImaging
        usdGeom
        tf
    CPPFILES
        testenv/testUsdImagingPrimvarUtils.cpp
)
pxr_build_test(testUsdImagingRerootingSceneIndex
    LIBRARIES
        usdImaging
        hd
        vt
    CPPFILES
        testenv/testUsdImagingRerootingSceneIndex.cpp
)
pxr_build_test(testUsdImagingRootPrim
    LIBRARIES
        usdImaging
        usdGeom
        usd
        hd
        gf
        arch
    CPPFILES
        testenv/testUsdImagingRootPrim.cpp
)
pxr_build_test(testUsdImagingPiPrototypeSceneIndex
    LIBRARIES
        usdImaging
        usdGeom
        usd
        sdf
        hd
        tf
    CPPFILES
        testenv/testUsdImagingPiPrototypeSceneIndex.cpp
)
pxr_build_test(testUsdImagingStageSceneIndex
    LIBRARIES
        usdImaging
        usdGeom
        usd
        sdf
        hd
        tf
    CPPFILES
        testenv/testUsdImagingStageSceneIndex.cpp
)
pxr_build_test(testUsdImagingStageSceneIndexContents
    LIBRARIES
        usdImaging
        hd
    CPPFILES
        testenv/testUsdImagingStageSceneIndexContents.cpp
)
pxr_build_test(testUsdImagingColorSpace
    LIBRARIES
        usdImaging
        hd
    CPPFILES
        testenv/testUsdImagingColorSpace.cpp
)
pxr_build_test(testUsdImagingInstanceProxyTraversal
    LIBRARIES
        usdImaging
        hd
        usd
        sdf
    CPPFILES
        testenv/testUsdImagingInstanceProxyTraversal.cpp
)
pxr_build_test(testUsdImagingCollectionPredicateLibrary
    LIBRARIES
        usdImaging
        hd
        usd
        kind
        tf
        sdf
    CPPFILES
        testenv/testUsdImagingCollectionPredicateLibrary.cpp
)

# Register tests to be run
pxr_register_test(testUsdImagingDataSourceAttribute
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingDataSourceAttribute"
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingDelegate
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingDelegate"
    TESTENV testenv/testUsdImagingDelegate
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingDelegateChanges
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingDelegateChanges"
    TESTENV testenv/testUsdImagingDelegateChanges
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingExcluded
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingExcluded"
    LABELS "requires_gpu"
)
# Tests that rely on plugins aren't currently supported in static builds.
if (BUILD_SHARED_LIBS)
    pxr_register_test(testUsdImagingMaterialBinding
        COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingMaterialBinding"
        TESTENV testenv/testUsdImagingMaterialBinding
        LABELS "requires_gpu"
    )
    pxr_register_test(testUsdImagingColorSpace
        COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingColorSpace"
        TESTENV testenv/testUsdImagingColorSpace
        LABELS "requires_gpu"
    )
endif()
pxr_register_test(testUsdImagingNestedInstancingCategories
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingNestedInstancingCategories"
    TESTENV testenv/testUsdImagingNestedInstancingCategories
    ENV
        USD_ASSIGN_PROTOTYPES_DETERMINISTICALLY=1
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingPrimvarUtils
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingPrimvarUtils"
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingRerootingSceneIndex
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingRerootingSceneIndex"
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingRootPrim
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingRootPrim"
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingPiPrototypeSceneIndex
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingPiPrototypeSceneIndex"
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingStageSceneIndex
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingStageSceneIndex"
    TESTENV testenv/testUsdImagingStageSceneIndex
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingStageSceneIndexContents
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingStageSceneIndexContents basic.usda basic.txt"
    TESTENV testenv/testUsdImagingStageSceneIndexContents
    DIFF_COMPARE
        basic.txt
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingInstanceProxyTraversal_1
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingInstanceProxyTraversal 1_simple.usda"
    TESTENV testenv/testUsdImagingInstanceProxyTraversal
    DIFF_COMPARE
        1_simple_usdTraversal.txt
        1_simple_sceneIndexTraversal.txt
        1_simple_sceneIndexInstanceProxyTraversal.txt
    ENV
        USD_ASSIGN_PROTOTYPES_DETERMINISTICALLY=1
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingInstanceProxyTraversal_2
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingInstanceProxyTraversal 2_ni-2-levels.usda"
    TESTENV testenv/testUsdImagingInstanceProxyTraversal
    DIFF_COMPARE
        2_ni-2-levels_usdTraversal.txt
        2_ni-2-levels_sceneIndexTraversal.txt
        2_ni-2-levels_sceneIndexInstanceProxyTraversal.txt
    ENV
        USD_ASSIGN_PROTOTYPES_DETERMINISTICALLY=1
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingCollectionPredicateLibrary
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingCollectionPredicateLibrary"
    LABELS "requires_gpu"
)

# This test requires MaterialX support and is not currently supported on static 
# builds as it uses a plugin mechanism which is not supported for static build 
# configurations. 
if (BUILD_SHARED_LIBS AND ${PXR_ENABLE_MATERIALX_SUPPORT})

pxr_build_test(testUsdImagingHdMtlx
    LIBRARIES
        tf
        hd
        hdMtlx
        usdImaging
    CPPFILES
        testenv/testUsdImagingHdMtlx.cpp
)
pxr_register_test(testUsdImagingHdMtlx_withMtlxVersion
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingHdMtlx --filename withMtlxVersion.usda"
    DIFF_COMPARE
        withMtlxVersion.mtlx
    TESTENV testenv/testUsdImagingHdMtlx
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingHdMtlx_withoutMtlxVersion
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingHdMtlx --filename withoutMtlxVersion.usda"
    DIFF_COMPARE
        withoutMtlxVersion.mtlx
    TESTENV testenv/testUsdImagingHdMtlx
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingHdMtlx_atan2Node
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingHdMtlx --filename atan2Node.usda"
    DIFF_COMPARE
        atan2Node.mtlx
    TESTENV testenv/testUsdImagingHdMtlx
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingHdMtlx_switchNode
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingHdMtlx --filename switchNode.usda"
    DIFF_COMPARE
        switchNode.mtlx
    TESTENV testenv/testUsdImagingHdMtlx
    LABELS "requires_gpu"
)
pxr_register_test(testUsdImagingHdMtlx_swizzleNode
    COMMAND "${CMAKE_INSTALL_PREFIX}/tests/testUsdImagingHdMtlx --filename swizzleNode.usda"
    DIFF_COMPARE
        swizzleNode.mtlx
    TESTENV testenv/testUsdImagingHdMtlx
    LABELS "requires_gpu"
)

endif() # BUILD_SHARED_LIBS AND PXR_ENABLE_MATERIALX_SUPPORT
