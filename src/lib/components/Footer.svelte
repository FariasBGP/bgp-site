<script lang="ts">
	import logoBGP from '$lib/img/BGP-branco-X.webp';
	import { Separator } from '$lib/components/ui/separator';
	import Facebook from 'lucide-svelte/icons/facebook';
	import Instagram from 'lucide-svelte/icons/instagram';
	import { Button } from './ui/button';
	import brazilImg from '$lib/img/mapaBrasil.webp';

	let anoAtual = new Date().getFullYear();
</script>

<footer
	class="flex min-h-[70%] w-full flex-col-reverse items-center justify-center gap-10 md:min-h-[50%] md:w-5/6 md:flex-row md:gap-0"
>
	<div
		class="flex h-full w-full flex-col items-center justify-center gap-3 md:w-1/4 md:items-start"
	>
		<div class="flex w-full items-center justify-center px-0 md:px-5">
			<img src={logoBGP} alt="Logo BGP Branco" class="w-80" />
		</div>
		<p class="hidden md:flex">Razao Social: Bgp Consultoria Ltda.</p>
		<p class="hidden md:flex">CNPJ: 29.432.186/0001-30</p>
		<div class="flex w-full justify-center gap-5 pb-10 pt-5 md:justify-start md:pb-0">
			<Button
				variant="ghost"
				target="_blank"
				class="px-1 py-6"
				href="https://www.instagram.com/bgpconsultoria/"
			>
				<Instagram size={40} />
			</Button>
			<Button
				target="_blank"
				variant="ghost"
				class="px-1 py-6"
				href="https://www.facebook.com/bgpconsultoria/?locale=pt_BR"
			>
				<Facebook size={40} />
			</Button>
		</div>
	</div>

	<Separator orientation="vertical" class="hidden min-h-[70%] md:flex" />

	<div class="flex w-full flex-col gap-5 p-5 text-center md:w-1/4">
		<p
			class="font-inter text-2xl font-semibold underline decoration-[#CB3E38] underline-offset-[6px]"
		>
			Quem somos
		</p>
		<p>
			Consultoria para provedores de internet e empresas que precisam de <span
				class="font-semibold text-[#CB3E38]">servidores estáveis</span
			>, seguros e de <span class="font-semibold text-[#CB3E38]">alto desempenho</span>.
		</p>
		<p>
			Aprimoramento da rede de internet com <span class="font-semibold text-[#CB3E38]"
				>diagnóstico técnico</span
			> preciso para melhorar a qualidade e performance no atendimento a clientes.
		</p>
	</div>
	<Separator orientation="vertical" class="hidden min-h-[70%] md:flex" />

	<div class="hidden w-2/4 items-center justify-center md:flex">
		<div class="flex w-1/2 flex-col items-center gap-5 text-pretty px-14 text-center">
			<p
				class="font-inter text-2xl font-semibold underline decoration-[#CB3E38] underline-offset-[6px]"
			>
				Contato
			</p>
			<p>
				Atendemos o <span class="font-semibold text-[#CB3E38]">Brasil inteiro</span> , entre em contato
				conosco para saber mais sobre nossos serviços.
			</p>
			<Button
				variant="outline"
				class="min-w-2/4 border-[#CB3E38]"
				href="https://wa.me/5511989111928?text=Ola%20Tudo%20bem%3F%0AOlhado%20o%20seu%20site%20e%20gostaria%20de%20saber%20mais!"
				target="_blank">(11) 98911-1928</Button
			>
		</div>
		<img src={brazilImg} alt="Mapa do brazil" class="w-1/2" />
	</div>
</footer>
