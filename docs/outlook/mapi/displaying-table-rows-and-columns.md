---
title: テーブルの行と列を表示します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ee60e64559a0b4163074ddb62ed72c4600c8e03d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799945"
---
# <a name="displaying-table-rows-and-columns"></a>テーブルの行と列を表示します。

  
  
**適用されます**: Outlook 
  
 新しい電子メールの受信者を定義するユーザーを有効にするのには、アドレス帳プロバイダーがプロパティ ページを使用できます。 
  
表示された対応する表には、コントロールごとに 1 つ、4 つの行が含まれています。 位置を示す列の値は次のとおりです。
  
|**Control**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|名前ラベルを表示  <br/> |14  <br/> |18  <br/> |49  <br/> |8  <br/> |
|表示名の編集] ボックス  <br/> |76  <br/> |16  <br/> |89  <br/> |12  <br/> |
|電子メール アドレスのラベル  <br/> |14  <br/> |42  <br/> |50  <br/> |8  <br/> |
|電子メール アドレスの編集] ボックス  <br/> |76  <br/> |40  <br/> |89  <br/> |12  <br/> |
|チェック ボックス  <br/> |14  <br/> |64  <br/> |90  <br/> |12  <br/> |
   
この次の表では、コントロールの種類、 **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) のプロパティ、および、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティのフラグのビットマスクの適切な値を示しています。
  
|**Control**|**型**|**Flags**|
|:-----|:-----|:-----|
|名前ラベルを表示  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|表示名の編集] ボックス  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|電子メール アドレスのラベル  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|電子メール アドレスの編集] ボックス  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|チェック ボックス  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
最後の表は、各コントロールを関連付けられているコントロールの構造体の内容です。 直接次の構造体のメモリ内の各ラベルのコントロールの値が表示されることに注意してください。
  
|**Control**|**Structure**|
|:-----|:-----|
|名前ラベルを表示  <br/> |{sizeof(DTBLLABEL)、0}"表示名:"  <br/> |
|表示名の編集] ボックス  <br/> |{sizeof(DTBLEDIT)、0、80、PR_DISPLAY_NAME}  <br/> |
|電子メール アドレスのラベル  <br/> |{sizeof(DTBLLABEL)、0}"電子メール アドレス:"  <br/> |
|電子メール アドレスの編集] ボックス  <br/> |{sizeof(DTBLEDIT)、0、80、PR_EMAIL_ADDRESS}  <br/> |
|チェック ボックス  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> **[Ok]**、**キャンセル**、および**ヘルプ**のボタンは、表示された表には含まれません。 ユーザー ・ インタ フェースは、表示テーブルにないコントロールを追加することによって、ダイアログ ボックスにコンテキストを追加できます。 
  
## <a name="see-also"></a>関連項目



[表示テーブルの実装](display-table-implementation.md)

