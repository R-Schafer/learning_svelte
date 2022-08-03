<script>
	import FeedbackList from './components/FeedbackList.svelte'
	
	let feedback = [
		{
			id: 1,
			rating: 10,
			text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Molestias aut, repellat ipsum facere voluptate dicta obcaecati deserunt nobis suscipit eaque?'
		},
		{
			id: 2,
			rating: 5,
			text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Molestias aut, repellat ipsum facere voluptate dicta obcaecati deserunt nobis suscipit eaque?'
		},
		{
			id: 3,
			rating: 7,
			text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Molestias aut, repellat ipsum facere voluptate dicta obcaecati deserunt nobis suscipit eaque?'
		}
	]
	
</script>

<main>
	 <FeedbackList {feedback} />
</main>
