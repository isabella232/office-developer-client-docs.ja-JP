---
title: 標準フォーム動詞の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426122"
---
# <a name="implementing-standard-form-verbs"></a>標準フォーム動詞の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、ユーザーがメニューを選択したり、ボタンをクリックしたりしたときに実行される標準の動詞のセットを定義します。これは、すべてのフォーム閲覧者がサポートしている必要があります。 各動詞には、exchform で定義されている、識別のための定数が関連付けられています。H ヘッダーファイル。 次の表に、標準のフォーム動詞とそれらに関連付けられている定数を示します。
  
|**Verb**|**値**|
|:-----|:-----|
|Open  <br/> |EXCHIVERB_OPEN  <br/> |
|返信  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|全員へ返信  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|[転送]  <br/> |EXCHIVERB_FORWARD  <br/> |
|Print  <br/> |EXCHIVERB_PRINT  <br/> |
|名前を付けて保存  <br/> |EXCHIVERB_SAVEAS  <br/> |
|フォルダーへ投稿  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
ユーザーが動詞を選択するときには、フォームの imapiform の呼び出しで定数を渡します[::D overb](imapiform-doverb.md)メソッドは、対応するアクションを実行します。 
  
フォームビューアーから動詞にアクセスするだけでなく、ユーザーはフォームから直接動詞にアクセスすることもできます。 たとえば、一部のフォームオブジェクトでは、ユーザーがフォームを右クリックして、状況依存のメニューから [**印刷**] を選択することによって、 **print**動詞を呼び出すことができます。 
  

