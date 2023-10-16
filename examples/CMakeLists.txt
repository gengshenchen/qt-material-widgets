
# 添加Qt资源文件到项目
qt5_add_resources(QRC_FILES examples.qrc)

add_executable(examples-exe WIN32 MACOSX_BUNDLE
    appbarsettingseditor.cpp appbarsettingseditor.h
    appbarsettingsform.ui
    autocompletesettingseditor.cpp autocompletesettingseditor.h
    avatarsettingseditor.cpp avatarsettingseditor.h
    avatarsettingsform.ui
    badgesettingseditor.cpp badgesettingseditor.h
    badgesettingsform.ui
    checkboxsettingseditor.cpp checkboxsettingseditor.h
    checkboxsettingsform.ui
    circularprogresssettingseditor.cpp circularprogresssettingseditor.h
    circularprogresssettingsform.ui
    dialogsettingseditor.cpp dialogsettingseditor.h
    dialogsettingsform.ui
    drawersettingseditor.cpp drawersettingseditor.h
    drawersettingsform.ui
    fabsettingseditor.cpp fabsettingseditor.h
    fabsettingsform.ui
    flatbuttonsettingseditor.cpp flatbuttonsettingseditor.h
    flatbuttonsettingsform.ui
    iconbuttonsettingseditor.cpp iconbuttonsettingseditor.h
    iconbuttonsettingsform.ui
    main.cpp
    mainwindow.cpp mainwindow.h
    menusettingseditor.cpp menusettingseditor.h
    progresssettingseditor.cpp progresssettingseditor.h
    progresssettingsform.ui
    radiobuttonsettingseditor.cpp radiobuttonsettingseditor.h
    radiobuttonsettingsform.ui
    raisedbuttonsettingseditor.cpp raisedbuttonsettingseditor.h
    scrollbarsettingseditor.cpp scrollbarsettingseditor.h
    scrollbarsettingsform.ui
    slidersettingseditor.cpp slidersettingseditor.h
    slidersettingsform.ui
    snackbarsettingseditor.cpp snackbarsettingseditor.h
    snackbarsettingsform.ui
    tabssettingseditor.cpp tabssettingseditor.h
    tabssettingsform.ui
    textfieldsettingseditor.cpp textfieldsettingseditor.h
    textfieldsettingsform.ui
    togglesettingseditor.cpp togglesettingseditor.h
    togglesettingsform.ui
    ${QRC_FILES}
)
target_include_directories(examples-exe PRIVATE
    ../components
)

link_directories(../components/${CMAKE_BUILD_TYPE}/)

target_link_libraries(examples-exe PRIVATE
    materialui
    Qt5::Core
    Qt5::Gui
    Qt5::Widgets
)
