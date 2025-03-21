# SPDX-License-Identifier: CC0-1.0
# SPDX-FileCopyrightText: No rights reserved

project('flatter', 'c',
          license: 'CC0-1.0',
          version: '0.0.1',
    meson_version: '>= 1.0.0',
)

test_app = executable('flatter', 'main.c',
  dependencies: [dependency('gio-2.0'), dependency('gtk4')],
       install: true,
)

test('test-success', test_app,
  env: [
    'GDK_BACKEND=wayland,x11',
    'GSK_RENDERER=opengl',
    'GTK_A11Y=test',
  ],
)

