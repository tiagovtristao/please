subinclude("//test/build_defs")

please_repo_e2e_test(
    name = "test_rerun_test",
    expected_output = {
        "wibble_test.txt": "wibble wibble wibble\nwibble wibble wibble",
    },
    plz_command = "plz test --show_all_output //package:wibble 2>&1 | grep 'wibble wibble wibble' > wibble_test.txt && plz test --rerun --show_all_output //package:wibble 2>&1 | grep 'wibble wibble wibble' >> wibble_test.txt",
    repo = "test_repo",
)
