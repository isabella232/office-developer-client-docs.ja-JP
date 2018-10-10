---
title: ADORecordConstruction インターフェイス (ADO)
TOCTitle: ADORecordConstruction Interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44272067d8018836fd7eb3d6cfaa762780f69868
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477921"
---
# <a name="adorecordconstruction-interface-ado"></a>ADORecordConstruction インターフェイス (ADO)


**適用されます**Access 2013 |。Office 2013

**ADORecordConstruction** インターフェイスは、C/C++ アプリケーションで OLE DB **Row** から ADO **Record** オブジェクトを作成するために使用します。

このインターフェイスでは、以下のプロパティがサポートされています。

## <a name="properties"></a>プロパティ

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>値の設定のみ可能です。<br />
この ADO<strong>レコード</strong>オブジェクトの OLE DB<strong>の行</strong>オブジェクトのコンテナーを設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p>読み取り/書き込み。<br />
OLE DB<strong>の行</strong>のオブジェクトから/この ADO<strong>レコード</strong>オブジェクトを取得または設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>メソッド

なし

## <a name="events"></a>イベント

なし

## <a name="remarks"></a>備考

OLE DB**の行**オブジェクト (pRow)、ADO**レコード**オブジェクトの () の構築、ADO**レコード**オブジェクト (adoR) の金額を次の 3 つの基本的な操作を指定します。

1.  ADO **Record** オブジェクトを作成します。
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  **IADORecordConstruction** インターフェイスで **Record** オブジェクトを照会します。
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  呼び出す、 **IADORecordConstruction::put\_行**プロパティ メソッドは、ADO**レコード**オブジェクトの OLE DB**の行**オブジェクトを設定します。
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
結果として得られた **adoR** オブジェクトは、OLE DB **Row** から作成された ADO **Record** オブジェクトを表します。

ADO **Record** オブジェクトは、OLE DB **Row** オブジェクトのコンテナーからも作成できます。

## <a name="requirements"></a>必要条件

**バージョン:** ADO 2.0 以上

**ライブラリ:** msado15.dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

