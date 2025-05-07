<script lang="ts">
	import '../app.css';
	import {base} from '$app/paths';

	let { children } = $props();
</script>
<div class="navBar" id="mainNavBar">
	<a href="{base}/home">Home</a>
	<a href="{base}/login">login</a>
	<a href="{base}/devblog">Devblog</a>
  <a href="{base}/quiz">quiz</a>
	<!--&#9776; is the code for the 3 line menu button-->
  </div>

<style>
	.navBar{
  background-color: #fff; 

}

/*Floats each item to the left with padding of 14 & 16 px.
Removes the underline with text decoration = none.*/
.navBar a{
  float: left;
  color: grey;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
  font-family: Tahoma;
}

/*Background color change during hover state*/
.navBar a:hover{
  background-color: white;
  color: #009cde;
}
</style>
{@render children()}

	