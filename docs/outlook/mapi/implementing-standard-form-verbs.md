---
title: 標準フォーム動詞の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a85a3adcd2fab920e9cbbd39bdd7a5ad52f223db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600835"
---
# <a name="implementing-standard-form-verbs"></a>標準フォーム動詞の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、すべてのフォーム ビューアーがサポートする必要がある一連の標準動詞、またはユーザーがメニュー選択を行った場合、またはボタンをクリックするときに実行されるアクションを定義します。 各動詞には、EXCHFORM で定義された識別用に関連付けられた定数があります。H ヘッダー ファイル。 次の表に、標準フォーム動詞とその関連する定数を示します。
  
|**Verb**|**値**|
|:-----|:-----|
|開く  <br/> |EXCHIVERB_OPEN  <br/> |
|返信  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|全員へ返信  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|転送  <br/> |EXCHIVERB_FORWARD  <br/> |
|印刷  <br/> |EXCHIVERB_PRINT  <br/> |
|名前を付けて保存  <br/> |EXCHIVERB_SAVEAS  <br/> |
|フォルダーへ投稿  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
ユーザーが動詞を選択すると、その定数をフォームの [IMAPIForm::D oVerb](imapiform-doverb.md) メソッドに渡して、対応するアクションを実行します。 
  
フォーム ビューアーを介して動詞にアクセスする以外に、ユーザーはフォームから直接動詞にアクセスできます。 たとえば、一部のフォーム オブジェクトでは、フォームを右クリックし、コンテキストに依存するメニューから [印刷] を選択することで、ユーザーが **Print** 動詞を呼び出す場合があります。 
  

