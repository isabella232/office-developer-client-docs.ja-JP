---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: '最終更新日: 2017 年9月20日'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326945"
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
  
> 順番変換するメッセージへのポインター。 **lpmessage**の種類の定義については、「mapidefs.h」を参照してください。
    
 _pstm_
  
> 読み上げストリームを出力する[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイス。 
    
 _ulFlags_
  
>  順番コンバータの特定のアクションを示すフラグ。 
    
CCSF_8BITHEADERS
  
> コンバータでは8ビットヘッダーが許可されている必要があります。
    
CCSF_EMBEDDED_MESSAGE
  
> 送信/未送信の情報は、X 未送信の情報として保持されます。
    
CCSF_GLOBAL_MESSAGE
  
> コンバータは、国際メッセージ (EAI/RFC6530) を作成する必要があります。
    
CCSF_INCLUDE_BCC
  
> MAPI メッセージの BCC 受信者は、MIME ストリームに含める必要があります。
    
CCSF_NO_MSGID
  
> 送信メッセージには、メッセージ Id フィールドを含めないでください。
    
CCSF_NOHEADERS
  
> コンバーターは、外部メッセージのヘッダーを無視する必要があります。
    
CCSF_PLAIN_TEXT_ONLY
  
> コンバータは、プレーンテキストのみを送信する必要があります。
    
CCSF_SMTP
  
> コンバーターに SMTP メッセージが渡されています。 このフラグは常に設定する必要があります。
    
CCSF_USE_RTF
  
> コンバーターは、MIME メッセージの HTML から RTF 形式に変換する必要があります。
    
CCSF_USE_TNEF
  
> コンバーターは、MIME メッセージでトランスポートニュートラルカプセル化形式 (TNEF) 形式を使用する必要があります。
    
## <a name="return-values"></a>戻り値

E_INVALIDARG
  
> 無効なフラグが渡されたか、 *pmsg*または*pstm*が NULL です。 
    
## <a name="remarks"></a>解説

標準の Outlook メッセージの種類に対してのみサポートされています。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|mapimime .cpp  <br/> |ImportEMLToIMessage  <br/> |mfcmapi は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。  <br/> |
|mapimime .cpp  <br/> |ExportIMessageToEML  <br/> |mfcmapi は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。  <br/> |
   
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

