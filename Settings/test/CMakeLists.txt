cmake_minimum_required(VERSION 3.1 FATAL_ERROR)

set(INCLUDE_PATH
    "${DeviceSettings_SOURCE_DIR}/include"
    "${AVSCommon_SOURCE_DIR}/AVS/test"
    "${AVSCommon_SOURCE_DIR}/Utils/test"
    "${AVSCommon_SOURCE_DIR}/SDKInterfaces/test"
    "${CertifiedSender_SOURCE_DIR}/test")

set(TEST_DB_FILE "${DeviceSettings_SOURCE_DIR}/test/SQLiteDeviceSettingStorageTest.db")


discover_unit_tests("${INCLUDE_PATH}" "DeviceSettings" "${TEST_DB_FILE}")
