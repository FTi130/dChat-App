<script>
    import {username, user} from "./user";

    function signout() {
        user.leave();
        user.set('');
    }
</script>

<header>
    <h1>ну, чат</h1>
    {#if $username}
        <div class="user-bio">
            <span>
                <strong>{$username}</strong>
            </span>
            <img src={`https://avatars.dicebear.com/api/initials/${$username}.svg`} alt=" " />
        </div>
            <button class="signout-button" on:click={signout}>
                Выйти
            </button>

        {:else}
        <h3>Чат</h3>


        {/if}
</header>