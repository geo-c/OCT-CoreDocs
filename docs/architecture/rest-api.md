##### Status-Codes

| Code | Meaning |
|------|---------|
| <span class="green">200</span> | Request successful |
| <span class="green">201</span> | Created |
| <span class="green">204</span> | No Content |
| <span class="red">400</span> | Bad Request |
| <span class="red">401</span> | Unauthorized |
| <span class="red">403</span> | Forbidden |
| <span class="red">404</span> | Not found |
| <span class="red">500</span> | Internal Server Error |
| <span class="blue">501</span> | Not implemented |


##### Authentication

| Abbreviation | Description |
|--------------|-------------|
| `PA` | Public access |
| `UT` | User-Access-Token needed |
| `AT` | Admin-Access-Token needed |
| `AO` | Admin only |


##### Endpoints

| Code | Endpoint | Method | Headers | Query |
|------|----------|--------|---------|-------|
| <span class="green">201</span> | `/api/signup` | **POST** | PA | |
| <span class="blue">501</span> | `/api/reset` | **POST** | PA | |
| <span class="green">201</span> | `/api/admin/signup` | **POST** | PA | |
| <span class="green">201</span> | `/api/admin/login/:username/:password` | **GET** | PA | |
| <span class="green">200</span> | `/api/apps` | **GET** | AT, AO | |
| <span class="green">200</span> | `/api/apps/byDate/:date` | **GET** | AT, AO | |
| <span class="green">201</span> | `/api/apps/:app_hash/logs` | **GET** | PA | |
| <span class="green">201</span> | `/api/apps/:app_hash/logsByCategory` | **GET** | PA | |
| <span class="green">201</span> | `/api/apps/:app_hash/logsByDataset` | **GET** | PA | |
| <span class="green">201</span> | `/api/categories` | **GET** | PA | |
| <span class="green">201</span> | `/api/categories/:category_id/apps` | **GET** | PA | |
| <span class="green">201</span> | `/api/categories/byDate/:date` | **GET** | PA | |
| <span class="green">201</span> | `/api/categories/withDatasets` | **GET** | PA | |
| <span class="green">201</span> | `/api/categories/withDatasets/:category_id` | **GET** | PA | |
| <span class="green">201</span> | `/api/tdataset` | **GET** | PA | |
| <span class="green">201</span> | `/api/tdataset/:sd_id` | **GET** | PA | |
| <span class="green">201</span> | `/api/main_database` | **GET** | PA | |
| <span class="green">201</span> | `/api/database_all` | **GET** | PA | |
| <span class="green">201</span> | `/api/database_all/:username` | **GET** | PA | |
| <span class="green">201</span> | `/api/query/:category_name` | **GET** | PA | |
| <span class="green">204</span> | `/query/point/:lat/:lon/:dst` | **GET** | PA | |
| <span class="green">201</span> | `/api/dataset/:query_extern` | **GET** | PA | |
| <span class="green">204</span> | `/api/querycheck` | **POST** | PA | |
| <span class="green">201</span> | `/api/spatial/:md_id` | **GET** | PA | |
| <span class="green">201</span> | `/api/sub_database/:md_name` | **GET** | PA | |
| <span class="green">201</span> | `/api/submit` | **POST** | PA | |
| <span class="green">201</span> | `/api/update` | **POST** | PA | |
| <span class="green">200</span> | `/api/visitor` | **POST** | PA | |
| <span class="green">200</span> | `/api/visitors/:status/:value` | **GET** | PA | |
| <span class="green">200</span> | `/api/visitors/:status/:value/:timeFrom` | **GET** | PA | |
| <span class="green">200</span> | `/api/visitors/:status/:value/:timeFrom/:timeTo` | **GET** | PA | |


##### Required Data

<span class="green">/api/signup</span>

```
{
	app_name: "",
	app_description: "",
	email:address: "",
	first_name: "",
	last_name_: ""
	
}

```

<span class="green">/api/admin/signup</span>

```
{
	username: "",
	password: "",
	first_name: "",
	last_name_: "",
	email: ""
}

```

<span class="green">/api/submit</span>

```
{
	ds_type: "",
	ds_description: "",
	ds_host: "",
	ds_port: "",
	ds_instance: "",
	db_user: "",
	db_password: "",
	created_by: "",
	md_name: "",
	md_description: "",
	publisher: "",
	published: "",
	license: "",
	sd_name: "",
	sd_description: "",
	query_intern: "",
	query_extern: "",
	query_description: "",
	categories: [""]
}

```

<span class="green">/api/update</span>

```
{
	ds_id: "",
	ds_type: "",
	ds_description: "",
	ds_host: "",
	ds_port: "",
	ds_instance: "",
	db_user: "",
	db_password: "",
	created_by: "",
	md_id: "",
	md_name: "",
	md_description: "",
	publisher: "",
	published: "",
	license: "",
	sd_name: "",
	sd_description: "",
	query_id: "",
	active: "",
	query_intern: "",
	query_extern: "",
	query_description: "",
	categories: [""]

}

```

<span class="green">/api/visitor</span>

```
{
	city: "",
	country_code: "",
	latitude: "",
	longitude: "",
	metro_code: "",
	region_code: "",
	time_zone: "",
	zip_code: ""
}

```
