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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432318"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MIME オブジェクトと MAPI メッセージ間の変換を許可します。 これは、インターネットを通してメッセージを転送する場合に役立ちます。
  
|||
|:-----|:-----|
|提供元:  <br/> |CLSID_IConverterSession  <br/> |
|インターフェイス識別子:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |MAPI から MIME への変換時に、MAPI から MIME への変換であいまいなアドレスを解決するために使用するオプションの MAPI アドレス帳を指定します。  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |変換時に使用するエンコードを初期化します。  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |MIME ストリームを MAPI メッセージに変換します。  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |MAPI メッセージを MIME ストリームに変換します。  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |コンバーターが **MAPIToMIMEStm** で返す MIME ストリームのテキストの折り返し幅を設定します。  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |コンバーターが **MAPIToMIMEStm** で MIME ストリームを返す形式を設定します。  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |MAPI メッセージを MIME ストリームに変換するときに MAPI から MIME へのコンバーターが使用するオプションの文字セットを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

**MAPIToMIMEStm** を使用して変換を実行する前に **、SetEncoding** を呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPI-MIME 会話 API について](about-the-mapi-mime-conversion-api.md)
  
[MAPI 定数](mapi-constants.md)

