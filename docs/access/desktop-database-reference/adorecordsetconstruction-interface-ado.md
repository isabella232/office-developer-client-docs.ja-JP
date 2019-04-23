---
title: ADORecordsetConstruction インターフェイス (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281634"
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
<td><p><a href="chapter-property-ado.md">節</a></p></td>
<td><p>読み取り/書き込み可能。<br />

ADO <strong>Recordset</strong> オブジェクトに対する OLE DB <strong>Chapter</strong> オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>読み取り/書き込み可能。<br />

ADO <strong>Recordset</strong> オブジェクトに対する OLE DB <strong>RowPosition</strong> オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">行</a></p></td>
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

OLE DB **Rowset**オブジェクト (pRowset) (ado **recordset**オブジェクトの構造) () を指定すると、ado **recordset**オブジェクト (adors) の構造は次の3つの基本的な操作になります。

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

3. IADORecordsetConstruction::p ut\_rowset プロパティメソッドを呼び出して、ADO の Recordset オブジェクトの OLE DB Rowset オブジェクトを設定します。

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
これで、結果オブジェクトは、OLE DB **Rowset**オブジェクトから作成された ADO **Recordset**オブジェクトを表します。

ADO **Recordset** オブジェクトは、OLE DB **Chapter** または **RowPosition** オブジェクトから作成することもできます。

## <a name="requirements"></a>要件

- **バージョン:** ADO 2.0 以上

- **ライブラリ:** msado15.dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

