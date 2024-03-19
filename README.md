```bash
❯ bazel build //src:tar    
INFO: Analyzed target //src:tar (0 packages loaded, 4 targets configured).
ERROR: /home/scott/dev/ncr/pkg_thing/src/BUILD.bazel:26:8: Writing: bazel-out/k8-fastbuild/bin/src/tar.tar failed: (Exit 1): build_tar failed: error executing PackageTar command (from target //src:tar) bazel-out/k8-opt-exec-ST-13d3ddad9198/bin/external/rules_pkg/pkg/private/tar/build_tar '--output=bazel-out/k8-fastbuild/bin/src/tar.tar' '--mode=0555' '--owner=0.0' '--owner_name=.' '--directory=/' ... (remaining 2 arguments skipped)

Use --sandbox_debug to see verbose messages from the sandbox and retain the sandbox build root for debugging
Traceback (most recent call last):
  File "/tmp/bazel-working-directory/_main/bazel-out/k8-opt-exec-ST-13d3ddad9198/bin/external/rules_pkg/pkg/private/tar/build_tar.runfiles/_main/../rules_pkg/pkg/private/tar/build_tar.py", line 459, in <module>
    main()
  File "/tmp/bazel-working-directory/_main/bazel-out/k8-opt-exec-ST-13d3ddad9198/bin/external/rules_pkg/pkg/private/tar/build_tar.runfiles/_main/../rules_pkg/pkg/private/tar/build_tar.py", line 450, in main
    output.add_manifest_entry(entry, file_attributes)
  File "/tmp/bazel-working-directory/_main/bazel-out/k8-opt-exec-ST-13d3ddad9198/bin/external/rules_pkg/pkg/private/tar/build_tar.runfiles/_main/../rules_pkg/pkg/private/tar/build_tar.py", line 332, in add_manifest_entry
    self.add_file(entry.src, entry.dest, **attrs)
  File "/tmp/bazel-working-directory/_main/bazel-out/k8-opt-exec-ST-13d3ddad9198/bin/external/rules_pkg/pkg/private/tar/build_tar.runfiles/_main/../rules_pkg/pkg/private/tar/build_tar.py", line 104, in add_file
    self.tarfile.add_file(
  File "/tmp/bazel-working-directory/_main/bazel-out/k8-opt-exec-ST-13d3ddad9198/bin/external/rules_pkg/pkg/private/tar/build_tar.runfiles/rules_pkg/pkg/private/tar/tar_writer.py", line 242, in add_file
    with open(file_content, 'rb') as f:
         ^^^^^^^^^^^^^^^^^^^^^^^^
IsADirectoryError: [Errno 21] Is a directory: 'bazel-out/k8-fastbuild/bin/src/bundle'
Target //src:tar failed to build
Use --verbose_failures to see the command lines of failed build steps.
INFO: Elapsed time: 0.123s, Critical Path: 0.07s
INFO: 3 processes: 3 internal.
ERROR: Build did NOT complete successfully
```
