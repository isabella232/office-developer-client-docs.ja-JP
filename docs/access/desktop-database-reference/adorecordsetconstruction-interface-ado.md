---
title: ADORecordsetConstruction インターフェイス (ADO)
TOCTitle: ADORecordsetConstruction Interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0b99fcfe4fadc3dddf5937ba1043875de43e88d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478520"
---
# <a name="adorecordsetconstruction-interface-ado"></a>ADORecordsetConstruction インターフェイス (ADO)


**適用されます**Access 2013 |。Office 2013

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
<td><p><a href="chapter-property-ado.md">章</a></p></td>
<td><p>読み取り/書き込み。<br />
<strong>章</strong>の OLE DB オブジェクトから/この ADO<strong>レコード セット</strong>オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>読み取り/書き込み。<br />
OLE DB <strong>RowPosition</strong>オブジェクトから/この ADO<strong>レコード セット</strong>オブジェクトを取得または設定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">行セット</a></p></td>
<td><p>読み取り/書き込み。<br />
/に ADO<strong>レコード セット</strong>オブジェクトには、OLE DB<strong>行セット</strong>オブジェクトを取得または設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>メソッド

なし

## <a name="events"></a>イベント

なし

## <a name="remarks"></a>備考

次の 3 つの基本的な操作を OLE DB の**行セット**オブジェクトのため、ADO**レコード セット**オブジェクトの () の構築、ADO**レコード セット**のオブジェクト (どちら) 金額の構築を指定します。

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

3. IADORecordsetConstruction::put を呼び出す\_ADO レコード セット オブジェクトの OLE DB 行セット オブジェクトを設定するのには行セット プロパティのメソッド。

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
これで、結果のオブジェクトは、OLE DB**行セット**オブジェクトから作成された ADO**レコード セット**オブジェクトを表します。

ADO **Recordset** オブジェクトは、OLE DB **Chapter** または **RowPosition** オブジェクトから作成することもできます。

## <a name="requirements"></a>必要条件

- **バージョン:** ADO 2.0 以上

- **ライブラリ:** msado15.dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

