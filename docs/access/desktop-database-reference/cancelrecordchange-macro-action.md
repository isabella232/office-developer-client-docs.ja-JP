---
title: CancelRecordChange マクロ アクション
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ebbde6cee79aa822d710089d06aff39767413ccc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606969"
---
# <a name="cancelrecordchange-macro-action"></a>CancelRecordChange マクロ アクション


**適用先**: Access 2013、Office 2013

You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.


> [!NOTE]
> The **CancelRecordChange** action is available only in Data Macros.



## <a name="remarks"></a>注釈

"**CancelRecordChange/レコードの変更の取り消し**" アクションを呼び出すと、**CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。

