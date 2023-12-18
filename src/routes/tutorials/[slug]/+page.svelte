<script lang="ts">
	import hljs from 'highlight.js/lib/core';
	import { CodeBlock } from '@skeletonlabs/skeleton';
	import bash from 'highlight.js/lib/languages/bash';

	hljs.registerLanguage('bash', bash);

	export let data;
</script>

<section class="max-w-2xl m-auto px-5">
	<h1 class="h1">{data.slug}</h1>

	<h2 class="h2">Launch Minikube:</h2>

	<p>Deploying Applications: Use kubectl to deploy applications. For example:</p>
	<CodeBlock language="bash" code={`minikube start`} />
	<p>This command will start the Minikube VM and Kubernetes cluster.</p>

	<p>Check the Status:</p>
	<CodeBlock language="bash" code={`minikube status`} />
	<p>This will show you the status of Minikube and the Kubernetes cluster.</p>
</section>
