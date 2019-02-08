
package(default_visibility = ["//visibility:public"])
load("//tensorflow/compiler/aot:tfcompile.bzl", "tf_library")

# Use the tf_library macro to compile your graph into executable code.
tf_library(
    name = "neurocontrol",
    cpp_class = "foo::bar::NeuralAttitudeModel",
    graph = "frozen_model_optimized.pb",
    config = "tf2xla.config.pbtxt",

	# Extra flags for compiler
#    target_triple = "arm-arm-none-eabi",

)

cc_binary(
    name="my_binary",
    deps = [

    ":neurocontrol"
    ]
    )

