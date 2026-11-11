<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- Face recognition runs in the browser via @vladmandic/face-api (src/lib/face.ts, dynamically imported); descriptors are stored on public.people — keeps biometrics off the server runtime.
- Roles live in public.user_roles (admin/gerente/usuario); first signup becomes admin via trigger.
