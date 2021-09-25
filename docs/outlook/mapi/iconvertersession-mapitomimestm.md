---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: '最終更新日: 2017 年 9 月 20 日'
ms.openlocfilehash: 563f83d6ebb76659afa99e446378b8d68a8e80b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613948"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI メッセージを MIME ストリームに変換します。
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>パラメーター

 _pmsg_
  
> [in]変換するメッセージへのポインター。 LPMESSAGE の型定義については、mapidefs.h **を参照してください**。
    
 _pstm_
  
> [out] [ストリームを](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 出力する IStream インターフェイス。 
    
 _ulFlags_
  
>  [in]コンバーターの特定のアクションを示すフラグ。 
    
CCSF_8BITHEADERS
  
> コンバーターは 8 ビット ヘッダーを許可する必要があります。
    
CCSF_EMBEDDED_MESSAGE
  
> 送信/送信されていない情報は X-Unsent に保持されます。
    
CCSF_GLOBAL_MESSAGE
  
> コンバーターは、国際メッセージ (EAI/RFC6530) を作成する必要があります。
    
CCSF_INCLUDE_BCC
  
> MAPI メッセージの BCC 受信者は MIME ストリームに含める必要があります。
    
CCSF_NO_MSGID
  
> 送信メッセージにMessage-Idフィールドを含めない。
    
CCSF_NOHEADERS
  
> コンバーターは、外部メッセージのヘッダーを無視する必要があります。
    
CCSF_PLAIN_TEXT_ONLY
  
> コンバーターはプレーン テキストを送信する必要があります。
    
CCSF_SMTP
  
> コンバーターは SMTP メッセージを渡されています。 このフラグは常に設定する必要があります。
    
CCSF_USE_RTF
  
> コンバーターは、MIME メッセージで HTML から RTF 形式に変換する必要があります。
    
CCSF_USE_TNEF
  
> コンバーターは、MIME メッセージでトランスポート ニュートラル カプセル化形式 (TNEF) 形式を使用する必要があります。
    
## <a name="return-values"></a>戻り値

E_INVALIDARG
  
> 無効なフラグが渡されたか  *、pmsg*  または  *pstm が*  NULL です。 
    
## <a name="remarks"></a>注釈

標準のメッセージの種類でのみOutlookサポートされます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI は MimeToMAPI を使用して EML ファイルを MAPI メッセージに変換します。  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI は MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
  
[PidTagMessageEditorFormat 標準プロパティ](pidtagmessageeditorformat-canonical-property.md)
  
[PidLidUseTnef ���K���̃v���p�e�B](pidlidusetnef-canonical-property.md)


[MAPI 定数](mapi-constants.md)

