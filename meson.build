project('google_benchmark', 'cpp', version: '???', default_options: ['cpp_std=c++14'])

inc = include_directories('include')

thread_dep = dependency('threads')

src = ['src/benchmark.cc',
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
   'src/timers.cc']

lib_static  = static_library('google_benchmark', src,
   include_directories : inc, dependencies: thread_dep)

lib_dynamic = shared_library('google_benchmark', src,
   include_directories : inc, dependencies: thread_dep)

benchmark_dep_static = declare_dependency(include_directories : inc,
                                          link_with : lib_static)

benchmark_dep_dynamic = declare_dependency(include_directories : inc, link_with : lib_dynamic)
