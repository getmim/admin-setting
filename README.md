# admin-setting

Adalah frontpage untuk halaman setting di dashboard admin.

## Instalasi

Jalankan perintah di bawah di folder aplikasi:

```
mim app install admin-setting
```

## Konfigurasi

Masing-masing module yang ingin menambahkan menu pada halaman setting harus menambahkan
konfigurasi pada module/aplikasi seperti di bawah:

```php
return [
    'adminSetting' => [
        'menus' => [
            '/id/' => [
                'label' => '/Menu Label/',
                'icon'  => '/menu icon in html/',
                'info'  => '/Description about the menu/',
                'perm'  => '/permission for checker/',
                'index' => 1,
                'options' => [
                    '/id/' => [
                        'label' => '/option label/',
                        'route' => ['routeName', [], []]
                    ],
                    // ...
                ]
            ]
        ]
    ]
];
```