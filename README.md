### ctest_debug

Runs ctest in debug mode
- status: 0
```
+ ctest --output-on-failure -E test-opt
Test project /Users/ggml/work/llama.cpp/build-ci-debug
      Start  1: test-quantize-fns
 1/12 Test  #1: test-quantize-fns ................   Passed    0.39 sec
      Start  2: test-quantize-perf
 2/12 Test  #2: test-quantize-perf ...............   Passed    0.41 sec
      Start  3: test-sampling
 3/12 Test  #3: test-sampling ....................   Passed    0.21 sec
      Start  4: test-tokenizer-0-llama
 4/12 Test  #4: test-tokenizer-0-llama ...........   Passed    0.32 sec
      Start  5: test-tokenizer-0-falcon
 5/12 Test  #5: test-tokenizer-0-falcon ..........   Passed    0.86 sec
      Start  6: test-tokenizer-1-llama
 6/12 Test  #6: test-tokenizer-1-llama ...........   Passed   13.19 sec
      Start  7: test-tokenizer-1-falcon
 7/12 Test  #7: test-tokenizer-1-falcon ..........   Passed   14.82 sec
      Start  8: test-tokenizer-1-aquila
 8/12 Test  #8: test-tokenizer-1-aquila ..........   Passed   17.09 sec
      Start  9: test-grammar-parser
 9/12 Test  #9: test-grammar-parser ..............   Passed    0.21 sec
      Start 10: test-llama-grammar
10/12 Test #10: test-llama-grammar ...............   Passed    0.21 sec
      Start 11: test-grad0
11/12 Test #11: test-grad0 .......................   Passed    1.04 sec
      Start 12: test-rope
12/12 Test #12: test-rope ........................   Passed    0.26 sec

100% tests passed, 0 tests failed out of 12

Total Test time (real) =  49.00 sec

real	0m49.048s
user	0m46.280s
sys	0m0.788s
```

### ctest_release

Runs ctest in release mode
- status: 0
```
+ ctest --output-on-failure
Test project /Users/ggml/work/llama.cpp/build-ci-release
      Start  1: test-quantize-fns
 1/12 Test  #1: test-quantize-fns ................   Passed    0.10 sec
      Start  2: test-quantize-perf
 2/12 Test  #2: test-quantize-perf ...............   Passed    0.08 sec
      Start  3: test-sampling
 3/12 Test  #3: test-sampling ....................   Passed    0.05 sec
      Start  4: test-tokenizer-0-llama
 4/12 Test  #4: test-tokenizer-0-llama ...........   Passed    0.07 sec
      Start  5: test-tokenizer-0-falcon
 5/12 Test  #5: test-tokenizer-0-falcon ..........   Passed    0.16 sec
      Start  6: test-tokenizer-1-llama
 6/12 Test  #6: test-tokenizer-1-llama ...........   Passed    1.73 sec
      Start  7: test-tokenizer-1-falcon
 7/12 Test  #7: test-tokenizer-1-falcon ..........   Passed    1.23 sec
      Start  8: test-tokenizer-1-aquila
 8/12 Test  #8: test-tokenizer-1-aquila ..........   Passed    1.44 sec
      Start  9: test-grammar-parser
 9/12 Test  #9: test-grammar-parser ..............   Passed    0.09 sec
      Start 10: test-llama-grammar
10/12 Test #10: test-llama-grammar ...............   Passed    0.05 sec
      Start 11: test-grad0
11/12 Test #11: test-grad0 .......................   Passed    0.83 sec
      Start 12: test-rope
12/12 Test #12: test-rope ........................   Passed    0.11 sec

100% tests passed, 0 tests failed out of 12

Total Test time (real) =   5.95 sec

real	0m5.969s
user	0m4.660s
sys	0m0.716s
```
### open_llama_3b_v2

OpenLLaMA 3B-v2:
- status: 134
- perplexity:

- lora:

- f16: 
```
+ ./bin/main --model ../models-mnt/open-llama/3B-v2/ggml-model-f16.gguf -s 1234 -n 64 --ignore-eos -p 'I believe the meaning of life is'
Log start
main: build = 1372 (b016596)
main: built with Apple clang version 14.0.3 (clang-1403.0.22.14.1) for arm64-apple-darwin22.5.0
main: seed  = 1234
llama_model_loader: loaded meta data with 18 key-value pairs and 237 tensors from ../models-mnt/open-llama/3B-v2/ggml-model-f16.gguf (version GGUF V2 (latest))
llama_model_loader: - tensor    0:                token_embd.weight f16      [  3200, 32000,     1,     1 ]
llama_model_loader: - tensor    1:              blk.0.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor    2:              blk.0.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor    3:              blk.0.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor    4:         blk.0.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor    5:            blk.0.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor    6:            blk.0.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor    7:              blk.0.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor    8:           blk.0.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor    9:            blk.0.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   10:              blk.1.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   11:              blk.1.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   12:              blk.1.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   13:         blk.1.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   14:            blk.1.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   15:            blk.1.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   16:              blk.1.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   17:           blk.1.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   18:            blk.1.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   19:              blk.2.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   20:              blk.2.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   21:              blk.2.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   22:         blk.2.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   23:            blk.2.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   24:            blk.2.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   25:              blk.2.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   26:           blk.2.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   27:            blk.2.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   28:              blk.3.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   29:              blk.3.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   30:              blk.3.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   31:         blk.3.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   32:            blk.3.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   33:            blk.3.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   34:              blk.3.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   35:           blk.3.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   36:            blk.3.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   37:              blk.4.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   38:              blk.4.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   39:              blk.4.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   40:         blk.4.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   41:            blk.4.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   42:            blk.4.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   43:              blk.4.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   44:           blk.4.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   45:            blk.4.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   46:              blk.5.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   47:              blk.5.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   48:              blk.5.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   49:         blk.5.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   50:            blk.5.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   51:            blk.5.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   52:              blk.5.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   53:           blk.5.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   54:            blk.5.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   55:              blk.6.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   56:              blk.6.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   57:              blk.6.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   58:         blk.6.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   59:            blk.6.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   60:            blk.6.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   61:              blk.6.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   62:           blk.6.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   63:            blk.6.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   64:              blk.7.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   65:              blk.7.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   66:              blk.7.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   67:         blk.7.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   68:            blk.7.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   69:            blk.7.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   70:              blk.7.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   71:           blk.7.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   72:            blk.7.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   73:              blk.8.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   74:              blk.8.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   75:              blk.8.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   76:         blk.8.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   77:            blk.8.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   78:            blk.8.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   79:              blk.8.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   80:           blk.8.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   81:            blk.8.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   82:              blk.9.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   83:              blk.9.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   84:              blk.9.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   85:         blk.9.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   86:            blk.9.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   87:            blk.9.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   88:              blk.9.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   89:           blk.9.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   90:            blk.9.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   91:             blk.10.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   92:             blk.10.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   93:             blk.10.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   94:        blk.10.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor   95:           blk.10.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   96:           blk.10.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor   97:             blk.10.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor   98:          blk.10.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor   99:           blk.10.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  100:             blk.11.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  101:             blk.11.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  102:             blk.11.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  103:        blk.11.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  104:           blk.11.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  105:           blk.11.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  106:             blk.11.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  107:          blk.11.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  108:           blk.11.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  109:             blk.12.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  110:             blk.12.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  111:             blk.12.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  112:        blk.12.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  113:           blk.12.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  114:           blk.12.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  115:             blk.12.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  116:          blk.12.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  117:           blk.12.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  118:             blk.13.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  119:             blk.13.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  120:             blk.13.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  121:        blk.13.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  122:           blk.13.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  123:           blk.13.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  124:             blk.13.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  125:          blk.13.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  126:           blk.13.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  127:             blk.14.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  128:             blk.14.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  129:             blk.14.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  130:        blk.14.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  131:           blk.14.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  132:           blk.14.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  133:             blk.14.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  134:          blk.14.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  135:           blk.14.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  136:             blk.15.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  137:             blk.15.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  138:             blk.15.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  139:        blk.15.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  140:           blk.15.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  141:           blk.15.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  142:             blk.15.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  143:          blk.15.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  144:           blk.15.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  145:             blk.16.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  146:             blk.16.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  147:             blk.16.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  148:        blk.16.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  149:           blk.16.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  150:           blk.16.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  151:             blk.16.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  152:          blk.16.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  153:           blk.16.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  154:             blk.17.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  155:             blk.17.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  156:             blk.17.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  157:        blk.17.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  158:           blk.17.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  159:           blk.17.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  160:             blk.17.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  161:          blk.17.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  162:           blk.17.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  163:             blk.18.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  164:             blk.18.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  165:             blk.18.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  166:        blk.18.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  167:           blk.18.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  168:           blk.18.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  169:             blk.18.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  170:          blk.18.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  171:           blk.18.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  172:             blk.19.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  173:             blk.19.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  174:             blk.19.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  175:        blk.19.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  176:           blk.19.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  177:           blk.19.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  178:             blk.19.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  179:          blk.19.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  180:           blk.19.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  181:             blk.20.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  182:             blk.20.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  183:             blk.20.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  184:        blk.20.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  185:           blk.20.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  186:           blk.20.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  187:             blk.20.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  188:          blk.20.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  189:           blk.20.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  190:             blk.21.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  191:             blk.21.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  192:             blk.21.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  193:        blk.21.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  194:           blk.21.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  195:           blk.21.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  196:             blk.21.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  197:          blk.21.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  198:           blk.21.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  199:             blk.22.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  200:             blk.22.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  201:             blk.22.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  202:        blk.22.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  203:           blk.22.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  204:           blk.22.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  205:             blk.22.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  206:          blk.22.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  207:           blk.22.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  208:             blk.23.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  209:             blk.23.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  210:             blk.23.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  211:        blk.23.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  212:           blk.23.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  213:           blk.23.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  214:             blk.23.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  215:          blk.23.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  216:           blk.23.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  217:             blk.24.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  218:             blk.24.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  219:             blk.24.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  220:        blk.24.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  221:           blk.24.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  222:           blk.24.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  223:             blk.24.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  224:          blk.24.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  225:           blk.24.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  226:             blk.25.attn_q.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  227:             blk.25.attn_k.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  228:             blk.25.attn_v.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  229:        blk.25.attn_output.weight f16      [  3200,  3200,     1,     1 ]
llama_model_loader: - tensor  230:           blk.25.ffn_gate.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  231:           blk.25.ffn_down.weight f16      [  8640,  3200,     1,     1 ]
llama_model_loader: - tensor  232:             blk.25.ffn_up.weight f16      [  3200,  8640,     1,     1 ]
llama_model_loader: - tensor  233:          blk.25.attn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  234:           blk.25.ffn_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  235:               output_norm.weight f32      [  3200,     1,     1,     1 ]
llama_model_loader: - tensor  236:                    output.weight f16      [  3200, 32000,     1,     1 ]
llama_model_loader: - kv   0:                       general.architecture str     
llama_model_loader: - kv   1:                               general.name str     
llama_model_loader: - kv   2:                       llama.context_length u32     
llama_model_loader: - kv   3:                     llama.embedding_length u32     
llama_model_loader: - kv   4:                          llama.block_count u32     
llama_model_loader: - kv   5:                  llama.feed_forward_length u32     
llama_model_loader: - kv   6:                 llama.rope.dimension_count u32     
llama_model_loader: - kv   7:                 llama.attention.head_count u32     
llama_model_loader: - kv   8:              llama.attention.head_count_kv u32     
llama_model_loader: - kv   9:     llama.attention.layer_norm_rms_epsilon f32     
llama_model_loader: - kv  10:                          general.file_type u32     
llama_model_loader: - kv  11:                       tokenizer.ggml.model str     
llama_model_loader: - kv  12:                      tokenizer.ggml.tokens arr     
llama_model_loader: - kv  13:                      tokenizer.ggml.scores arr     
llama_model_loader: - kv  14:                  tokenizer.ggml.token_type arr     
llama_model_loader: - kv  15:                tokenizer.ggml.bos_token_id u32     
llama_model_loader: - kv  16:                tokenizer.ggml.eos_token_id u32     
llama_model_loader: - kv  17:            tokenizer.ggml.padding_token_id u32     
llama_model_loader: - type  f32:   53 tensors
llama_model_loader: - type  f16:  184 tensors
llm_load_print_meta: format           = GGUF V2 (latest)
llm_load_print_meta: arch             = llama
llm_load_print_meta: vocab type       = SPM
llm_load_print_meta: n_vocab          = 32000
llm_load_print_meta: n_merges         = 0
llm_load_print_meta: n_ctx_train      = 2048
llm_load_print_meta: n_embd           = 3200
llm_load_print_meta: n_head           = 32
llm_load_print_meta: n_head_kv        = 32
llm_load_print_meta: n_layer          = 26
llm_load_print_meta: n_rot            = 100
llm_load_print_meta: n_gqa            = 1
llm_load_print_meta: f_norm_eps       = 0.0e+00
llm_load_print_meta: f_norm_rms_eps   = 1.0e-06
llm_load_print_meta: f_clamp_kqv      = 0.0e+00
llm_load_print_meta: f_max_alibi_bias = 0.0e+00
llm_load_print_meta: n_ff             = 8640
llm_load_print_meta: freq_base_train  = 10000.0
llm_load_print_meta: freq_scale_train = 1
llm_load_print_meta: model type       = 3B
llm_load_print_meta: model ftype      = mostly F16
llm_load_print_meta: model params     = 3.43 B
llm_load_print_meta: model size       = 6.38 GiB (16.00 BPW) 
llm_load_print_meta: general.name   = open-llama
llm_load_print_meta: BOS token = 1 '<s>'
llm_load_print_meta: EOS token = 2 '</s>'
llm_load_print_meta: UNK token = 0 '<unk>'
llm_load_print_meta: PAD token = 0 '<unk>'
llm_load_print_meta: LF token  = 13 '<0x0A>'
llm_load_tensors: ggml ctx size =    0.08 MB
llm_load_tensors: mem required  = 6535.88 MB
.................................................................................................
llama_new_context_with_model: n_ctx      = 512
llama_new_context_with_model: freq_base  = 10000.0
llama_new_context_with_model: freq_scale = 1
llama_new_context_with_model: kv self size  =  162.50 MB
ggml_metal_init: allocating
ggml_metal_init: found device: Apple M1
ggml_metal_init: picking default device: Apple M1
ggml_metal_init: default.metallib not found, loading from source
ggml_metal_init: loading '/Users/ggml/work/llama.cpp/build-ci-release/bin/ggml-metal.metal'
ggml_metal_init: loaded kernel_add                            0x146807040 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_add_row                        0x146807ae0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul                            0x146808000 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_row                        0x146808650 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_scale                          0x11eb08800 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_silu                           0x11eb08c00 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_relu                           0x146808a50 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_gelu                           0x11eb09000 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_soft_max                       0x11eb09920 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_soft_max_4                     0x146809130 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_diag_mask_inf                  0x1468098d0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_diag_mask_inf_8                0x14680a240 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_f32                   0x14680a980 | th_max =  896 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_f16                   0x14680b050 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_q4_0                  0x11eb0a060 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_q4_1                  0x14680b600 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_q8_0                  0x14680bdf0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_q2_K                  0x14680c4c0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_q3_K                  0x14680cb90 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_q4_K                  0x11eb0a600 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_q5_K                  0x14680d3d0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_get_rows_q6_K                  0x14680daa0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_rms_norm                       0x14680e180 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_norm                           0x14680eb30 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_f32_f32                 0x14680f5d0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_f16_f32                 0x14680fe50 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_f16_f32_1row            0x11eb0b1c0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_f16_f32_l4              0x11eb0bbc0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_q4_0_f32                0x1468104b0 | th_max =  896 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_q4_1_f32                0x146810d70 | th_max =  896 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_q8_0_f32                0x146811610 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_q2_K_f32                0x146811d90 | th_max =  640 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_q3_K_f32                0x1468122b0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_q4_K_f32                0x146812ad0 | th_max =  896 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_q5_K_f32                0x146813250 | th_max =  832 | th_width =   32
ggml_metal_init: loaded kernel_mul_mv_q6_K_f32                0x11eb0c220 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_f32_f32                 0x146812ed0 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_f16_f32                 0x146814340 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_q4_0_f32                0x11eb0ca80 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_q8_0_f32                0x11eb0d400 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_q4_1_f32                0x146814a50 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_q2_K_f32                0x11eb0db10 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_q3_K_f32                0x1468152b0 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_q4_K_f32                0x146815c00 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_q5_K_f32                0x11eb0e340 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_mul_mm_q6_K_f32                0x146816310 | th_max =  768 | th_width =   32
ggml_metal_init: loaded kernel_rope_f32                       0x11eb0e030 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_rope_f16                       0x11eb0f1b0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_alibi_f32                      0x11eb0f6d0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_cpy_f32_f16                    0x11eb102f0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_cpy_f32_f32                    0x11eb10ba0 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_cpy_f16_f16                    0x11eb11450 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_concat                         0x146816000 | th_max = 1024 | th_width =   32
ggml_metal_init: loaded kernel_sqr                            0x146816830 | th_max = 1024 | th_width =   32
ggml_metal_init: GPU name:   Apple M1
ggml_metal_init: GPU family: MTLGPUFamilyApple7 (1007)
ggml_metal_init: hasUnifiedMemory              = true
ggml_metal_init: recommendedMaxWorkingSetSize  =  5461.34 MB
ggml_metal_init: maxTransferRate               = built-in GPU
llama_new_context_with_model: compute buffer total size = 74.88 MB
llama_new_context_with_model: max tensor size =   195.31 MB
ggml_metal_add_buffer: allocated 'data            ' buffer, size =  4096.00 MB, offs =            0
ggml_metal_add_buffer: allocated 'data            ' buffer, size =  2635.86 MB, offs =   4090150912, ( 6732.36 /  5461.34), warning: current allocated size is greater than the recommended max working set size
ggml_metal_add_buffer: allocated 'kv              ' buffer, size =   164.50 MB, ( 6896.86 /  5461.34), warning: current allocated size is greater than the recommended max working set size
ggml_metal_add_buffer: allocated 'alloc           ' buffer, size =    68.77 MB, ( 6965.62 /  5461.34), warning: current allocated size is greater than the recommended max working set size
ggml_metal_graph_compute: command buffer 2 failed with status 5
GGML_ASSERT: /Users/ggml/work/llama.cpp/ggml-metal.m:1459: false
ci/run.sh: line 237: 11592 Abort trap: 6           ./bin/main --model ${model_f16} -s 1234 -n 64 --ignore-eos -p "I believe the meaning of life is"
```
- q8_0:
```

```
- q4_0:
```

```
- q4_1:
```

```
- q5_0:
```

```
- q5_1:
```

```
- q2_k:
```

```
- q3_k:
```

```
- q4_k:
```

```
- q5_k:
```

```
- q6_k:
```

```
- shakespeare (f16):
```

```
- shakespeare (f16 lora):
```

```
- shakespeare (q8_0):
```

```
- shakespeare (q8_0 lora):
```

```
- shakespeare (q8_0 / f16 base lora):
```

```
