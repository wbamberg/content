---
title: IDBEnvironmentSync
slug: Web/API/IDBEnvironmentSync
tags:
  - API
  - Experimental
  - IndexedDB
  - Interface
  - Deprecated
  - Reference
---
{{APIRef("IndexedDB")}} {{ draft() }}

> **Warning:** The synchronous version of the IndexedDB API was originally intended for use only with [Web Workers](/en-US/docs/Web/API/Web_Workers_API/Using_web_workers), and was eventually removed from the spec because its need was questionable. It may however be reintroduced in the future if there is enough demand from web developers.

The {{ unimplemented_inline() }} `IDBEnvironmentSync` interface of the [IndexedDB API](/en-US/docs/Web/API/IndexedDB_API) will be implemented by [worker](/en-US/docs/Web/API/Worker) objects.

## Attributes

<table class="standard-table">
  <thead>
    <tr>
      <th scope="col">Attribute</th>
      <th scope="col">Type</th>
      <th scope="col">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>indexedDBSync</code></td>
      <td>
        <code
          >readonly
          <a href="/en-US/docs/Web/API/IDBFactorySync">IDBFactorySync</a></code
        >
      </td>
      <td>
        Provides a synchronous means of accessing the capabilities of indexed
        databases.
        <div class="notecard note">
          <p>
            <strong>Note:</strong> Until the Indexed Database API specification
            is finalized, this attribute should be accessed as
            <code>moz_indexedDBSync</code>.
          </p>
        </div>
      </td>
    </tr>
  </tbody>
</table>
