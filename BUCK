python_binary(
  name = 'tailer',
  main_module = 'tailer',
  deps = [
    ':tailerutils',
  ],
)

genrule(
  name = 'lstailer',
  cmd = 'tree * > $OUT',
  srcs = [
    ':tailerutils', # this does not work :(
    # ':tailer', # this works as expected
  ],
  out = 'lstailer.txt'
)

python_library(
  name = 'tailerutils',
  # The main module, tailer.py, is specified here.
  # (Separated out from the glob pattern for clarity.)
  srcs = glob(['tailer.py', '*.py']),
)
