---
title: レコードセット関連のエラー情報
TOCTitle: Recordset-Related Error Information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2df186db80515fdc9a7e77b8030d3ccd82ad793
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888700"
---
# <a name="recordset-related-error-information"></a>レコードセット関連のエラー情報


**適用されます**Access 2013、Office 2013。

バッチ処理中に、 **Recordset** オブジェクトの **Status** プロパティにより、 **Recordset** 内の個別のレコードに関する情報が表示されます。 バッチ更新が行われる前に、 **Recordset** の **Status** プロパティには、追加、変更、および削除されるレコードに関する情報が反映されます。 

**UpdateBatch** が呼び出された後、 **Status** プロパティは、操作の成功または失敗を示します。 **Recordset** 内のレコード間を移動すると、 **Status** プロパティの値が現在のレコードのステータスを示す値に変わります。

