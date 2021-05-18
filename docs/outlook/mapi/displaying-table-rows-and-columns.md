---
title: テーブルの行と列の表示
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f9f1cc0bebf3c90a5c12f2714e8ab7eea59104da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407117"
---
# <a name="displaying-table-rows-and-columns"></a>テーブルの行と列の表示

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 アドレス帳プロバイダーは、プロパティ ページを使用して、ユーザーが新しい電子メール受信者を定義できます。 
  
対応する表示テーブルには、コントロールごとに 1 行の 4 行が含まれます。 位置を示す列の値は次のとおりです。
  
|**Control**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|表示名ラベル  <br/> |14   <br/> |18   <br/> |49  <br/> |8  <br/> |
|[表示名] 編集ボックス  <br/> |76  <br/> |16   <br/> |89  <br/> |12   <br/> |
|電子メール アドレス ラベル  <br/> |14   <br/> |42  <br/> |50  <br/> |8  <br/> |
|[電子メール アドレスの編集] ボックス  <br/> |76  <br/> |40  <br/> |89  <br/> |12   <br/> |
|チェック ボックス  <br/> |14   <br/> |64  <br/> |90  <br/> |12   <br/> |
   
次の表は、コントロールの型、 **その PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) プロパティ、およびフラグのビットマスク 、その PR_CONTROL_FLAGS **(** [PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに適切な値を示します。
  
|**Control**|**Type**|**Flags**|
|:-----|:-----|:-----|
|表示名ラベル  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|[表示名] 編集ボックス  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|電子メール アドレス ラベル  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|[電子メール アドレスの編集] ボックス  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|チェック ボックス  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
最後の表には、関連付けられたコントロール構造の内容を含む各コントロールが一覧表示されます。 各ラベル コントロールの値は、構造体の直下のメモリに表示されます。
  
|**Control**|**Structure**|
|:-----|:-----|
|表示名ラベル  <br/> |{sizeof(DTBLLABEL), 0}"表示名:"  <br/> |
|[表示名] 編集ボックス  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|電子メール アドレス ラベル  <br/> |{sizeof(DTBLLABEL), 0}"Email address:"  <br/> |
|[電子メール アドレスの編集] ボックス  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|チェック ボックス  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> **[OK]、[****キャンセル**]、**および [ヘルプ**] ボタンは、表示テーブルには含まれません。 ユーザー インターフェイスは、表示テーブルではなくコントロールを追加することで、ダイアログ ボックスにコンテキストを追加できます。 
  
## <a name="see-also"></a>関連項目



[表示テーブルの実装](display-table-implementation.md)

