set(krunner_ssh_SRCS
    ssh.cpp
)

add_library(krunner_ssh MODULE ${krunner_ssh_SRCS})
target_link_libraries(krunner_ssh KF5::Runner KF5::Plasma Qt5::Widgets Qt5::Xml
    KF5::I18n KF5::Service KF5::KIOCore KF5::KIOFileWidgets KF5::KIOWidgets KF5::KIONTLM)
install(TARGETS krunner_ssh DESTINATION ${PLUGIN_INSTALL_DIR})
install(FILES plasma-runner-ssh.desktop DESTINATION ${SERVICES_INSTALL_DIR})
