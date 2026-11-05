# CarPlay vehicle artwork

Vehicle photos, transparent cutouts, template cars and brand logos exported from CarPlay_Radio.

`manifest.json` maps stable application asset identifiers to immutable `objects/<SHA-256>.<extension>` files, including byte sizes and integrity hashes. Download objects individually; keep existing objects when publishing updates so older app versions continue working.

The app bundles the small manifest and vehicle catalogue, downloads artwork on demand, verifies SHA-256 and persists verified images for offline reuse. It does not bundle these artwork files. A first-time download requires network access.

To update from the app repository:

```sh
python3 tool/sync_remote_vehicle_assets.py /path/to/car_database
```

Source metadata is preserved under `assets/`. Logos and trademarks belong to their respective owners; hosting does not change the original artwork rights.
