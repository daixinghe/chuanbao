- Rancher 
admin/approaching
- Higress 30848
admin/qujing@3a8e2165a7e694f9
Mock key ：api_7b165f4e4420dbeccb51309796df26c5 1
- Grafana 30080
admin/wIlsBAhDI0xKaosJy6f9sZAoGFLJ7P8Lbh0LCFfM
wdcc/T7HGMhwHx8tsM34x7KKt
wdcc_sa/glsa_ouNAAOU9aeEWjb6fV67JBVUNfVL5l3Ff_2b714c57
- Console  8080
admin/30d60ba30b8e0eae
- ATaas api  3000
admin/12345678
https://10.255.87.120:3000




QUlMQwEhHpNqAAAAACGrumoAAAAAAAAAAJoratkeGt_IE2wgOpCC20WmRkjSTNk-NwkH0aG7SRQRynRr3V00d6Qr6Lt2xBerZAoAY3VzdG9tZXItMQ.Xy3eFs9-0u1F1tLUJA-7n6QBx_Z8KrEMDF-qcM5kqcoKmJ63ajr5OH3ECJ59EI7zPiJ7vTFP2xUKSBzlIeeFAA


QUlMQwEhNqhqAAAAACHDz2oAAAAAAAAAAGGnqUDiezu2LMclbNv-4TVHo5DnvJAs82Kkg0o4jK89-H4zeLyF6zGnJo-1qgYEegoAY3VzdG9tZXItMQ.xJsCmhtA4t0Su4PlKSJlxkcFZLBauKRkJPio1HzkyO3MEPj3G__seqoJOwaRzxTeNU9ymYdfzWzLUOMtuleNBA


[2026-10-03 02:21:28 DP5 TP5 EP5] Scheduler hit an exception: Traceback (most recent call last):
  File "/sgl-workspace/sglang/python/sglang/srt/managers/scheduler.py", line 3943, in run_scheduler_process
    scheduler.run_event_loop()
  File "/sgl-workspace/sglang/python/sglang/srt/managers/scheduler.py", line 1390, in run_event_loop
    dispatch_event_loop(self)
  File "/sgl-workspace/sglang/python/sglang/srt/managers/scheduler.py", line 3833, in dispatch_event_loop
    scheduler.event_loop_overlap_disagg_decode()
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/_contextlib.py", line 120, in decorate_context
    return func(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^
  File "/sgl-workspace/sglang/python/sglang/srt/disaggregation/decode.py", line 1221, in event_loop_overlap_disagg_decode
    batch_result = self.run_batch(batch)
                   ^^^^^^^^^^^^^^^^^^^^^
  File "/sgl-workspace/sglang/python/sglang/srt/managers/scheduler.py", line 2918, in run_batch
    batch_result = self.model_worker.forward_batch_generation(
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/sgl-workspace/sglang/python/sglang/srt/speculative/eagle_worker_v2.py", line 752, in forward_batch_generation
    self.draft_worker._draft_extend_for_decode(
  File "/sgl-workspace/sglang/python/sglang/srt/speculative/eagle_worker_v2.py", line 592, in _draft_extend_for_decode
    draft_logits_output = self.draft_runner.forward(
                          ^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/sgl-workspace/sglang/python/sglang/srt/model_executor/model_runner.py", line 2740, in forward
    output = self._forward_raw(
             ^^^^^^^^^^^^^^^^^^
  File "/sgl-workspace/sglang/python/sglang/srt/model_executor/model_runner.py", line 2814, in _forward_raw
    forward_batch.prepare_mlp_sync_batch(self)
  File "/sgl-workspace/sglang/python/sglang/srt/model_executor/forward_batch_info.py", line 918, in prepare_mlp_sync_batch
    global_num_tokens_pinned = torch.tensor(global_num_tokens, pin_memory=True)
                               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
torch.AcceleratorError: CUDA error: unspecified launch failure
Search for `cudaErrorLaunchFailure' in https://docs.nvidia.com/cuda/cuda-runtime-api/group__CUDART__TYPES.html for more information.
CUDA kernel errors might be asynchronously reported at some other API call, so the stacktrace below might be incorrect.
For debugging consider passing CUDA_LAUNCH_BLOCKING=1
Compile with `TORCH_USE_CUDA_DSA` to enable device-side assertions.


[2026-10-03 02:21:29] Subprocess scheduler_0 (pid=1123) crashed with exit code -3. Triggering SIGQUIT for cleanup...
