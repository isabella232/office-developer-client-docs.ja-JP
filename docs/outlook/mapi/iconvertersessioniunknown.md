---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a89b1a93b2b03f97426a3988739e9b0d8411f113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800426"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**適用対象**: Outlook 
  
MIME オブジェクト、および MAPI メッセージ間の変換を使用できます。 これは、インターネット経由でメッセージの転送に便利なことができます。
  
|||
|:-----|:-----|
|提供元:  <br/> |CLSID_IConverterSession  <br/> |
|インターフェイスの識別子。  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |MAPI メッセージを MIME ストリームに変換するときにあいまいなアドレスを解決するのには MIME コンバーターに MAPI を使用して MAPI アドレス帳を指定します。  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |変換時に使用するエンコーディングを初期化します。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |MIME ストリームを MAPI メッセージに変換します。  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |MAPI メッセージを MIME ストリームに変換します。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |テキストの折り返しの MIME ストリームを表すコンバーター **MAPIToMIMEStm**の幅を設定します。  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |コンバーターには、 **MAPIToMIMEStm**の MIME ストリームを取得する書式を設定します。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |MIME コンバーターに MAPI が MAPI メッセージを MIME ストリームに変換するときに使用する、省略可能な文字の設定を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

**MAPIToMIMEStm**を使用して変換を実行する前に、 **SetEncoding**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPI-MIME 会話 API について](about-the-mapi-mime-conversion-api.md)
  
[MAPI �萔](mapi-constants.md)

