# MTJ-on-TPU_driver0.2

This is a modified mesh-transformer-jax adapted to JAX 0.3.25 so you can infer on colab with TPU_driver0.2.
You can continue to use the same (slim) weights as before.

Background;
In early March 2023, Google removed TPU_driver0.1 from colab. The original GPT-J strictly requires JAX 0.2.12 so it could not be inferred with on colab anymore because TPU_driver0.2 needs newer jax.

Takeaway;
I added some modifications to mesh_transformer folder and colab demo together with the updated requirements. Thus you can infer with this on colab now. You can continue to use the same (slim) weights as before.

How;
I uploaded the relevant file and folder here. You can extract mesh_transformer folder and requirement.txt file, replace them with the originals in your own repo, and use GPT-J inference on TPU_driver0.2.ipynb to infer with.

Important notes: 

1) Sorry, you'll need pro or pro+ subscription of colab because it requires high memory TPU runtime.

2) I have not checked it for finetuning on TPU VM. This can cause errors during a process.
I'm planning to cover it next month. Until then, possibly you must add further modifications to xmap by yourself or downgrade to jax 0.2.18 or 0.2.20.

3) You can also infer with GPT-J by device_serve.py on TPU VM, but you can't use the original file. If anyone wants it, please post a request from issue.

!Update on 4/28/2023!

Due to the python upgrade of colab (3.9 -> 3.10), requirements.txt and util.py were modified.
