# Enhancing code readability in Code

Using a nice color theme is just one of many tweaks you as a developer may use in order to enhance the code readability in Code.

Here are my tips for improving the appearance and code readability in Code:

> **Use a monospaced font supporting font ligatures.** The font used is probably just as important as the color theme when it comes to code readability.

If you haven't already switched to a monospaced font supporting font ligatures, please do so now and see for yourself. I personally use [FiraCode](https://github.com/tonsky/FiraCode) as my font of choice.

Relevant configuration in `settings.json`:

``` json
  "editor.fontFamily": "'FiraCode-Light'",
  "editor.fontLigatures": true,
```

> **Prefer naked code.** Turn off *everything* which distracts code readability. I do not need or want to see the number of references for a given type or version control information (such as Git author) injected into the code (this information is most likely always available from a keystroke command anyway).

For me this means:

- Turning off **References Code Lens for C#** (I do keep the Test Code Lens on)
- Turning off **Navigation breadcrumbs** in the editor header area
- Hiding **Indent guides**
- Hiding whitespace and/or control characters. These are off by default in Code anyway.
- Hiding version control information, such as Git metadata (possibly displayed if you are using an extension).

Relevant configuration in `settings.json`:

``` json
  "csharp.referencesCodeLens.enabled": false,
  "breadcrumbs.enabled": false,
  "editor.renderIndentGuides": false,
```

## Missing features in Code

Although Code is wonderful in most respects I have found some annoying glitches mostly having to do with the way Code converts language tokens and other content into grammar scopes (using [TextMate grammars](https://www.sublimetext.com/docs/3/scope_naming.html)).

Specifically for C#, Code exhibits the following shortcomings:

- Generic type parameters are scoped as `entity.name.type.type-parameter.cs` when defining a class of some type, but all later instances of the same parameter type is always scoped as `storage.type.cs`.

> I would prefer the color theme to be able to preserve the appearance of the type parameter throughout the class definition and I don't want `entity.name.type.type-parameter.cs` to have the same appearance as `storage.type.cs`. This is currently not possible AFAIK.

- Different keywords are always scoped as "storage.modifier". This makes it impossible to have some keywords stand out.

> It would be nice to have certain keywords such as `unsafe` stand out. This is currently not possible AFAIK (Note: version 1.0.3 now makes `unchecked` stand out).

- Function definitions and function calls are always scoped as `entity.name.function.cs`.

> It would be nice to be able to make function definitions stand out and differ from ordinary function calls (Other language grammars in Code, such as TypeScript, has additional scopes which separates function definitions from function calls).

## Creating your own color theme

I have used the following resources when creating this color theme:

- Official Code documentation: [Color Themes in Visual Studio Code](https://code.visualstudio.com/docs/getstarted/themes)
- [How to write a Visual Studio Code color theme from scratch (Medium)](https://medium.com/@caludio/how-to-write-a-visual-studio-code-color-theme-from-scratch-7ccb7e5da2aa)