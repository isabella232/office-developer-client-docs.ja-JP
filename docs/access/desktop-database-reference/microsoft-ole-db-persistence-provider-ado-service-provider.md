---
title: Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7b021daeb4d43be52d0b8c8409e3be866b8b27b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589366"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)


**適用先**: Access 2013、Office 2013 

Microsoft OLE DB Persistence Provider を使用すると、[Recordset](recordset-object-ado.md) オブジェクトをファイルに保存し、後でその **Recordset** オブジェクトをファイルから復元できます。スキーマ情報、データ、および保留中の変更が保持されます。

**Recordset** は、独自の ADTG (Advanced Data Table Gram) 形式または公開されている XML (Extensible Markup Language) 形式で保存できます。

## <a name="provider-keyword"></a>プロバイダー キーワード

このプロバイダーを呼び出すには、接続文字列で次のキーワードと値を指定します。

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>エラー

このプロバイダーからの次のエラーが発生し、アプリケーションで検出されることがあります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>E_BADSTREAM</p></td>
<td><p>開かれたファイルの形式が有効な形式 (ADTG 形式または XML 形式) ではありません。</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>保存する <strong>Recordset</strong> オブジェクトには、保存を妨げる特性があります。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Microsoft OLE DB Persistence Provider は動的プロパティを公開しません。

現在、パラメーター化された階層 **Recordset** オブジェクトのみ保存できません。

**Recordset** オブジェクトの永続的保存の詳細については、「[レコードセットの保存の詳細](more-about-recordset-persistence.md)」を参照してください。

ストリームを使用して **Recordset** を開く場合、**Open** メソッドの *Source* パラメーター以外のパラメーターは指定しないでください。

