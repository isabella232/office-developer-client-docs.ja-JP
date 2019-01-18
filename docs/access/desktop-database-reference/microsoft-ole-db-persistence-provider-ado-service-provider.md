---
title: Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715509"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)


**適用されます**Access 2013、Office 2013。 

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


## <a name="remarks"></a>解説

Microsoft OLE DB Persistence Provider は動的プロパティを公開しません。

現在、パラメーター化された階層 **Recordset** オブジェクトのみ保存できません。

**Recordset** オブジェクトの永続的保存の詳細については、「 [レコードセットの保存の詳細](more-about-recordset-persistence.md)」を参照してください。

ストリームが使用すると、**レコード セット**を開く必要がありますパラメーターが指定されていない、 **Open**メソッドの*Source*パラメーター以外の場合。

