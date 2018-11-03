---
title: レコード セットに関連するエラー情報
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b0dc56ba591263cd834e26ca4e89a371f272d5a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946469"
---
# <a name="recordset-related-error-information"></a>レコード セットに関連するエラー情報

**適用されます**Access 2013、Office 2013。

バッチ処理中に、 **Recordset** オブジェクトの **Status** プロパティにより、 **Recordset** 内の個別のレコードに関する情報が表示されます。 バッチ更新が行われる前に、 **Recordset** の **Status** プロパティには、追加、変更、および削除されるレコードに関する情報が反映されます。 

**UpdateBatch** が呼び出された後、 **Status** プロパティは、操作の成功または失敗を示します。 **Recordset** 内のレコード間を移動すると、 **Status** プロパティの値が現在のレコードのステータスを示す値に変わります。

