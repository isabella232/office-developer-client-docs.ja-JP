---
title: 既存レコードの編集
TOCTitle: Editing existing records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37da1e888eaa4231c58155e6830477f853b4027f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944670"
---
# <a name="editing-existing-records"></a>既存レコードの編集


**適用されます**Access 2013、Office 2013。

既存のレコードを編集するには、編集対象の行に移動し、変更するフィールドの **Value** プロパティを変更します。 **Field** オブジェクトの **Value** プロパティの詳細については、「 [3 章: データを調べる](chapter-3-examining-data.md)」を参照してください。変更をデータ ソースに送り返すには、カーソルの種類に応じ、 **Update** または **UpdateBatch** を使用します。詳細については、「 [5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

通常、更新や、その他の操作を実行するときは、ストアド プロシージャをコマンド オブジェクトと共に使用すると、より効率的です。これは、ストアド プロシージャがカーソルの作成を必要としないからです。カーソルの詳細については、「[8 章: カーソルとロックの概要](chapter-8-understanding-cursors-and-locks.md)」を参照してください。

