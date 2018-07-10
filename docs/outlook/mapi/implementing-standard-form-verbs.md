---
title: フォームの標準的な動詞を実装します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8135af7947f30ac600b8d9af364b2a79a3443ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800954"
---
# <a name="implementing-standard-form-verbs"></a>フォームの標準的な動詞を実装します。

  
  
**適用されます**: Outlook 
  
MAPI では、標準的な動詞、またはユーザーがメニュー アイテムを選択、またはフォームのすべてのビューアーをサポートする必要がありますボタンをクリックしたときに実行されたアクションのセットを定義します。 各動詞には、EXCHFORM で定義されている、識別用に、それに関連する定数です。H ヘッダー ファイルです。 次の表は、フォームの標準動詞と、関連付けられている定数の一覧。
  
|**動詞**|**値**|
|:-----|:-----|
|開く  <br/> |EXCHIVERB_OPEN  <br/> |
|Reply  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|全員へ返信  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Forward  <br/> |EXCHIVERB_FORWARD  <br/> |
|印刷  <br/> |EXCHIVERB_PRINT  <br/> |
|としてを保存します。  <br/> |EXCHIVERB_SAVEAS  <br/> |
|フォルダーへの返信  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
ユーザーが動詞を選択したときに対応するアクションを実行するのには、フォームの[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドの呼び出しでその定数を渡します。 
  
動詞にアクセスする、フォームのビューアーで、ほか、ユーザーはフォームから直接動詞をもアクセスできます。 などのいくつかのフォーム オブジェクトを許可すると、ユーザーがフォーム上を右クリックし、コンテキスト メニューから**印刷**を選択する**印刷**の動詞を呼び出します。 
  
