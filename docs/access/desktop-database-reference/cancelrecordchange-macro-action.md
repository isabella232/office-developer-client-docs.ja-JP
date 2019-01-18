---
title: CancelRecordChange マクロ アクション
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d19e7adcdd3bb60f24d90e75942fcc0b4e16e2e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718544"
---
# <a name="cancelrecordchange-macro-action"></a>CancelRecordChange マクロ アクション


**適用されます**Access 2013、Office 2013。

" **CancelRecordChange/レコードの変更の取り消し** " アクションを使用して、変更を確定する前に **[CreateRecord](createrecord-data-block.md)** または **[EditRecord](editrecord-data-block.md)** データ ブロック内でレコードに適用した変更を取り消すことができます。


> [!NOTE]
> [!メモ] " **CancelRecordChange/レコードの変更の取り消し** " アクションは、データ マクロ内でのみ使用できます。



## <a name="remarks"></a>解説

" **CancelRecordChange/レコードの変更の取り消し** " アクションを呼び出すと、 **CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。

