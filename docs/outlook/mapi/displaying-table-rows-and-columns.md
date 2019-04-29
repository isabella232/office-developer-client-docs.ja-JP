---
title: 表の行と列の表示
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
# <a name="displaying-table-rows-and-columns"></a>表の行と列の表示

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 プロパティページは、ユーザーが新しい電子メール受信者を定義できるように、アドレス帳プロバイダーが使用できます。 
  
対応する表示テーブルには、コントロールごとに1つずつ、4つの行が含まれています。 position を示す列の値は次のようになります。
  
|**Control**|**XPOS**|**YPOS**|**deltax**|**deltay**|
|:-----|:-----|:-----|:-----|:-----|
|表示名ラベル  <br/> |14   <br/> |18   <br/> |49  <br/> |8   <br/> |
|[表示名] 編集ボックス  <br/> |76  <br/> |16   <br/> |89  <br/> |12   <br/> |
|電子メールアドレスラベル  <br/> |14   <br/> |42  <br/> |50  <br/> |8   <br/> |
|メールアドレスの編集ボックス  <br/> |76  <br/> |40  <br/> |89  <br/> |12   <br/> |
|チェック ボックス  <br/> |14   <br/> |64  <br/> |90  <br/> |12   <br/> |
   
次の表は、コントロールの種類、 **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) プロパティ、フラグのビットマスク、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティの適切な値を示しています。
  
|**Control**|**Type**|**Flags**|
|:-----|:-----|:-----|
|表示名ラベル  <br/> |DTCT_LABEL  <br/> |.0  <br/> |
|[表示名] 編集ボックス  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|電子メールアドレスラベル  <br/> |DTCT_LABEL  <br/> |.0  <br/> |
|メールアドレスの編集ボックス  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|チェック ボックス  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
最後の表に、関連付けられたコントロール構造の内容を含む各コントロールの一覧を示します。 ラベルコントロールのそれぞれの値は、構造体のすぐ後のメモリに表示されることに注意してください。
  
|**Control**|**Structure**|
|:-----|:-----|
|表示名ラベル  <br/> |{sizeof (dtbllabel), 0}"表示名:"  <br/> |
|[表示名] 編集ボックス  <br/> |{sizeof (DTBLEDIT)、0、80、PR_DISPLAY_NAME}  <br/> |
|電子メールアドレスラベル  <br/> |{sizeof (dtbllabel), 0}"電子メールアドレス:"  <br/> |
|メールアドレスの編集ボックス  <br/> |{sizeof (DTBLEDIT)、0、80、PR_EMAIL_ADDRESS}  <br/> |
|チェック ボックス  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> **[OK]**、 **[キャンセル**]、[**ヘルプ**] の各ボタンは、表示テーブルに含まれていません。 ユーザーインターフェイスでは、表示テーブルにないコントロールを追加することによって、ダイアログボックスにコンテキストを追加することができます。 
  
## <a name="see-also"></a>関連項目



[表示テーブルの実装](display-table-implementation.md)

