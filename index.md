
## Default Variables

### homebrew_cask_accept_external_apps

Accept external cask apps

#### Default value

```yaml
homebrew_cask_accept_external_apps: false
```

### homebrew_cask_dir

Destination directory for casks

#### Default value

```yaml
homebrew_cask_dir: /Applications
```

### homebrew_casks

List of casks to install or uninstall

#### Default value

```yaml
homebrew_casks: []
```

#### Example usage

```yaml
homebrew_casks:
  - foo
  - name: bar
    greedy: True
    options: debug,appdir=/Applications
    accept_external_apps: True
    state: present
  - name: baz
    state: absent
```

### homebrew_clear_cache

Clear cache after installation

#### Default value

```yaml
homebrew_clear_cache: true
```

### homebrew_group

Group to run user-specific commands

#### Default value

```yaml
homebrew_group | default(ansible_user_gid)
```

### homebrew_packages

List of packages to install or uninstall

#### Default value

```yaml
homebrew_packages: []
```

#### Example usage

```yaml
homebrew_packages:
  - foo
  - name: bar
    greedy: True
    options: with-baz,enable-debug
    state: present
  - name: baz
    state: absent
```

### homebrew_taps

List of taps to install or uninstall

#### Default value

```yaml
homebrew_taps: []
```

#### Example usage

```yaml
homebrew_taps:
  - foo/bar
  - name: bar
    url: https://github.com/foo/bar
    state: present
  - name: foo/baz
    state: absent
```

### homebrew_user

User to run user-specific commands

#### Default value

```yaml
homebrew_user | default(ansible_user_id)
```
## Dependencies

None

## License

Apache-2.0

## Author

Thomas Boerger
