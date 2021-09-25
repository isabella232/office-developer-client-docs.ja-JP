---
title: ADORecordsetConstruction インターフェイス (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fb31007a8dc1a1471219a5849924e147aab41778
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559214"
---
# <a name="adorecordsetconstruction-interface-ado"></a>ADORecordsetConstruction インターフェイス (ADO)


**適用先:** Access 2013、Office 2013

. **ADORecordsetConstruction** インターフェイスは、C/C++ アプリケーションで OLE DB **Rowset** オブジェクトから ADO **Recordset** オブジェクトを作成するために使用されます。

このインターフェイスでは、以下のプロパティがサポートされています。

## <a name="properties"></a>プロパティ

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">チャプター</a></p></td>
<td><p>読み取り/書き込み可能。<br />

ADO <strong>Recordset</strong> オブジェクトに対する OLE DB <strong>Chapter</strong> オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>読み取り/書き込み可能。<br />

ADO <strong>Recordset</strong> オブジェクトに対する OLE DB <strong>RowPosition</strong> オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">行セット</a></p></td>
<td><p>読み取り/書き込み可能。<br />

ADO <strong>Recordset</strong> オブジェクトに対する OLE DB <strong>Rowset</strong> オブジェクトを取得または設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>メソッド

なし。

## <a name="events"></a>イベント

なし。

## <a name="remarks"></a>注釈

OLE DB **Rowset** オブジェクト (pRowset) を指定すると、ADO **Recordset** オブジェクト () の構築では、ADO **Recordset** オブジェクト (adoRs) の構築は、次の 3 つの基本的な操作になります。

1. ADO **Recordset** オブジェクトを作成します。
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. **IADORecordsetConstruction** インターフェイスで **Recordset** オブジェクトを照会します。

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. ADO Recordset オブジェクトに OLE DB Rowset オブジェクトを設定するには、IADORecordsetConstruction::p ut Rowset プロパティ メソッド \_ を呼び出します。

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
結果のオブジェクトは、OLE DB **Rowset** オブジェクトから構築された ADO Recordset オブジェクト **を表** します。

ADO **Recordset** オブジェクトは、OLE DB **Chapter** または **RowPosition** オブジェクトから作成することもできます。

## <a name="requirements"></a>要件

- **バージョン:** ADO 2.0 以上

- **ライブラリ:** msado15.dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

