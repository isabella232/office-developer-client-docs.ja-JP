---
title: ParentURL プロパティ (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 17d65b4b471172d08ce5868e78d43c8b101f1476
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617875"
---
# <a name="parenturl-property-ado"></a>ParentURL プロパティ (ADO)

**適用先**: Access 2013、Office 2013

現在の [Record](record-object-ado.md) オブジェクトの親 **Record** を示す絶対 URL 文字列を示します。

## <a name="return-value"></a>戻り値

親 **Record** の URL を示す文字列型 (**String**) の値を返します。

## <a name="remarks"></a>注釈

**ParentURL** プロパティは、 **Record** オブジェクトを開くために使用されるソースに依存します。たとえば、 **ActiveConnection** プロパティによって参照されるディレクトリの相対パスを含むソースを使用して [Record](activeconnection-property-ado.md) を開くことができます。

ここで、"second" が "first" の下のフォルダーであるとします。 **Record** オブジェクトを開くには、次のようにします。

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

**ここで、ParentURL** プロパティの値は **ParentURL** プロパティが " で https://first **、ActiveConnection と同じです**。

ソースには、"" などの絶対 URL を指定 https://first/second することもできます。 **ParentURL プロパティ** は https://first "" で、上記のレベルです。 **ParentURL プロパティ** は https://first "" で、"second" より上のレベルです。

次のような場合、このプロパティは Null 値になります。

- 現在のレコードに親がない場合 ( **Record** オブジェクトがディレクトリのルートを表す場合など)

- **Record** オブジェクトが URL で指定できないエンティティである場合

このプロパティは値の取得のみ可能です。


> [!NOTE]
> - [!メモ] このプロパティは、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) などのドキュメント ソース プロバイダーでのみサポートされます。詳細については、「 [レコードおよびプロバイダー提供のフィールド](records-and-provider-supplied-fields.md)」を参照してください。
> - [!メモ] http スキームを使用している URL は、Microsoft OLE DB Provider for Internet Publishing を自動的に呼び出します。 詳細については、「[絶対 URL と相対 URL](absolute-and-relative-urls.md)」を参照してください。 
> - [!メモ] 現在のレコードに ADO **Recordset** のデータ レコードが含まれている場合、 **ParentURL** プロパティにアクセスすると、URL を取得できないことを示す実行時エラーが発生します。


