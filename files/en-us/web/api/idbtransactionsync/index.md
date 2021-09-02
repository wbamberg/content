---
title: IDBTransactionSync
slug: Web/API/IDBTransactionSync
tags:
  - API
  - Experimental
  - IndexedDB
  - Interface
  - Deprecated
  - Reference
---
{{APIRef("IndexedDB")}}{{ draft() }}

> **Warning:** The synchronous version of the IndexedDB API was originally intended for use only with [Web Workers](/en-US/docs/Web/API/Web_Workers_API/Using_web_workers), and was eventually removed from the spec because its need was questionable. It may however be reintroduced in the future if there is enough demand from web developers.

The `IDBTransactionSync` interface of the [IndexedDB API](/en-US/docs/Web/API/IndexedDB_API) provides a synchronous [transaction](/en-US/docs/Web/API/IndexedDB_API/Basic_Terminology#transaction) on a database. When an application creates an IDBTransactionSync object, it blocks until the browser is able to reserve the require database objects.

## Method overview

<table class="standard-table">
  <tbody>
    <tr>
      <td>
        <code
          >void <a href="#abort">abort</a>() raises (<a
            href="/en-US/docs/Web/API/IDBDatabaseException"
            >IDBDatabaseException</a
          >);</code
        >
      </td>
    </tr>
    <tr>
      <td>
        <code
          >void <a href="#commit">commit</a>() raises (<a
            href="/en-US/docs/Web/API/IDBDatabaseException"
            >IDBDatabaseException</a
          >);</code
        >
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><a href="/en-US/docs/Web/API/IDBObjectStoreSync"
            >IDBObjectStoreSync</a
          >
          <a href="#objectstore">objectStore</a>(in DOMString name) raises (<a
            href="/en-US/docs/Web/API/IDBDatabaseException"
            >IDBDatabaseException</a
          >);</code
        >
      </td>
    </tr>
  </tbody>
</table>

## Attributes

| Attribute | Type                                                     | Description                                                                                                                                  |
| --------- | -------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `db`      | [`IDBDatabaseSync`](/en-US/docs/Web/API/IDBDatabaseSync) | The [database connection](/en-US/docs/Web/API/IndexedDB_API/Basic_Terminology#database_connection) that this transaction is associated with. |
| `static`  | `boolean`                                                | If true, this transaction is static; if false, this transaction is dynamic.                                                                  |

## Methods

### abort()

Call this method to signal a need to cancel the effects of the operations performed by this transaction. When this method is called, the browser ignores all the changes performed to the objects of this database since this transaction was created.

    void abort(
    ) raises (IDBDatabaseException);

##### Exceptions

This method can raise an IDBDatabaseException with the following code:

- [`NON_TRANSIENT_ERR`](/en-US/docs/Web/API/IDBDatabaseException#non_transient_err)
  - : If this transaction has already been committed or aborted.

### commit()

Call this method to signal that the transaction has completed normally and satisfactorily. When this method is called, the browser durably stores all the changes performed to the objects of the database since this transaction was created.

    void commit(
    ) raises (IDBDatabaseException);

##### Exceptions

This method can raise an IDBDatabaseException with the following codes:

- [`NON_TRANSIENT_ERR`](/en-US/docs/Web/API/IDBDatabaseException#non_transient_err)
  - : If this transaction has already been committed or aborted.
- [`RECOVERABLE_ERR`](/en-US/docs/Web/API/IDBDatabaseException#recoverable_err)
  - : If this transaction's scope is dynamic, and the browser cannot commit all of the changes due to another transaction.

### objectStore()

Returns an [object store](/en-US/docs/Web/API/IndexedDB_API/Basic_Terminology#object_store) that has already been added to the scope of this transaction.

    IDBObjectStoreSync objectStore(
      in DOMString name
    ) raises (IDBDatabaseException);

##### Parameters

- name
  - : The name of the requested object store.

##### Returns

- [`IDBObjectStoreSync`](/IDBObjectStoreSync)
  - : An object for accessing the requested object store.

##### Exceptions

The method can raise an IDBDatabaseException with the following code:

- [`NOT_FOUND_ERR`](/en-US/docs/Web/API/IDBDatabaseException#not_found_err)
  - : If the requested object store is not in this transaction's scope.
