if( EOSIO_COMPILE_TEST_CONTRACTS )
   add_contract( eosio.bios eosio.bios eosio.bios.cpp )
else()
   configure_file( ${CMAKE_CURRENT_SOURCE_DIR}/eosio.bios.wasm ${CMAKE_CURRENT_BINARY_DIR}/eosio.bios.wasm COPYONLY )
   configure_file( ${CMAKE_CURRENT_SOURCE_DIR}/eosio.bios.abi  ${CMAKE_CURRENT_BINARY_DIR}/eosio.bios.abi  COPYONLY )
endif()
