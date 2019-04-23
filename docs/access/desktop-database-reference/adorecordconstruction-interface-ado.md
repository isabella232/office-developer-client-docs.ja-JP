---
title: ADORecordConstruction インターフェイス (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281627"
---
# <a name="adorecordconstruction-interface-ado"></a>ADORecordConstruction インターフェイス (ADO)


**適用先:** Access 2013、Office 2013

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
<td><p>書き込み専用です。<br />

ADO <strong>Record</strong> オブジェクトに対する OLE DB <strong>Row</strong> オブジェクトのコンテナーを設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">行</a></p></td>
<td><p>読み取り/書き込み可能。<br />

ADO <strong>Record</strong> オブジェクトに対する OLE DB <strong>Row</strong> オブジェクトを取得または設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>メソッド

なし。

## <a name="events"></a>イベント

なし。

## <a name="remarks"></a>注釈

OLE DB **Row**オブジェクト (prow)、ado record オブジェクト (adoR) の**** 構造、および次の3つの基本的な**** 操作に対する金額を指定します。

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

3.  **IADORecordConstruction::p ut\_row**プロパティメソッドを呼び出して、ADO **Record**オブジェクトの OLE DB **Row**オブジェクトを設定します。
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
結果として得られた **adoR** オブジェクトは、OLE DB **Row** から作成された ADO **Record** オブジェクトを表します。

ADO **Record** オブジェクトは、OLE DB **Row** オブジェクトのコンテナーからも作成できます。

## <a name="requirements"></a>要件

**バージョン:** ADO 2.0 以上

**ライブラリ:** msado15.dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

