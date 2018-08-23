---
title: 標準のフォーム動詞の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 46585859e1dde4ecf38262f99cac5e3a9d29e5db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568750"
---
# <a name="implementing-standard-form-verbs"></a>標準のフォーム動詞の実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI では、標準的な動詞、またはユーザーがメニュー アイテムを選択、またはフォームのすべてのビューアーをサポートする必要がありますボタンをクリックしたときに実行されたアクションのセットを定義します。 各動詞には、EXCHFORM で定義されている、識別用に、それに関連する定数です。H ヘッダー ファイルです。 次の表は、フォームの標準動詞と、関連付けられている定数の一覧。
  
|**動詞**|**値**|
|:-----|:-----|
|Open  <br/> |EXCHIVERB_OPEN  <br/> |
|Reply  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|全員へ返信  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Forward  <br/> |EXCHIVERB_FORWARD  <br/> |
|印刷  <br/> |EXCHIVERB_PRINT  <br/> |
|としてを保存します。  <br/> |EXCHIVERB_SAVEAS  <br/> |
|フォルダーへ投稿  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
ユーザーが動詞を選択したときに対応するアクションを実行するのには、フォームの[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドの呼び出しでその定数を渡します。 
  
動詞にアクセスする、フォームのビューアーで、ほか、ユーザーはフォームから直接動詞をもアクセスできます。 などのいくつかのフォーム オブジェクトを許可すると、ユーザーがフォーム上を右クリックし、コンテキスト メニューから**印刷**を選択する**印刷**の動詞を呼び出します。 
  

