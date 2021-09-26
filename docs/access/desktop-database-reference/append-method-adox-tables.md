---
title: Append メソッド (ADOX Tables)
TOCTitle: Append method (ADOX Tables)
ms:assetid: 9e9fd57c-a856-6179-013f-9f378c3b7df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249726(v=office.15)
ms:contentKeyID: 48546664
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cc98da0c565da6e21f6ac58e6ee19a482402fe68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607340"
---
# <a name="append-method-adox-tables"></a>Append メソッド (ADOX Tables)

**適用先**: Access 2013、Office 2013

新しい [Table](table-object-adox.md) オブジェクトを [Tables](tables-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*テーブル*.Append *Table*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Table* | 追加する **Table** への参照を含むバリアント型 ( **Variant** ) の値、または作成して追加するテーブルの名前を指定します。|

## <a name="remarks"></a>注釈

プロバイダーがテーブルの作成をサポートしていない場合は、エラーが発生します。

