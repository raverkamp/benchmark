project('google_benchmark', 'cpp', version: '???', default_options: ['cpp_std=c++14'])

inc = include_directories('include')

thread_dep = dependency('threads')

lib = library('google_benchmark',
  ['src/benchmark.cc',
   'src/commandlineflags.cc',
   'src/csv_reporter.cc',
   'src/statistics.cc',
   'src/benchmark_main.cc',
   'src/complexity.cc',
   'src/json_reporter.cc',
   'src/string_util.cc',
   'src/benchmark_register.cc',
   'src/console_reporter.cc',
   'src/reporter.cc',
   'src/sysinfo.cc',
   'src/colorprint.cc',
   'src/counter.cc',
   'src/sleep.cc',
   'src/timers.cc'],
   include_directories : inc, dependencies: thread_dep)

benchmark_dep = declare_dependency(include_directories : inc, link_with : lib)
