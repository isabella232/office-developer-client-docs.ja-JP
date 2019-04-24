---
title: iconvertersession IUnknown
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
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336688"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MIME オブジェクトと MAPI メッセージ間の変換を可能にします。 これは、インターネット経由でメッセージを転送する場合に役立ちます。
  
|||
|:-----|:-----|
|提供元:  <br/> |CLSID_IConverterSession  <br/> |
|インターフェイス識別子:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|**[setadrbook](iconvertersession-setadrbook.md)** <br/> |mapi メッセージを mime ストリームに変換するときに、あいまいなアドレスを解決するために mapi から mime コンバータが使用するオプションの mapi アドレス帳を指定します。  <br/> |
|**[setencoding](iconvertersession-setencoding.md)** <br/> |変換時に使用するエンコードを初期化します。  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |MIME ストリームを MAPI メッセージに変換します。  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |MAPI メッセージを MIME ストリームに変換します。  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |**MAPIToMIMEStm**でコンバータが返す MIME ストリームのテキストの折り返し幅を設定します。  <br/> |
|**[setsaveformat](iconvertersession-setsaveformat.md)** <br/> |コンバーターが**MAPIToMIMEStm**で MIME ストリームを返す形式を設定します。  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
|**[setcharset](iconvertersession-setcharset.md)** <br/> |mapi メッセージを mime ストリームに変換するときに mapi から mime コンバータが使用するオプションの文字セットを指定します。  <br/> |
   
## <a name="remarks"></a>解説

**MAPIToMIMEStm**を使用して変換を実行する前に、 **setencoding**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPI-MIME 会話 API について](about-the-mapi-mime-conversion-api.md)
  
[MAPI 定数](mapi-constants.md)

