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
description: '最終更新日: 2017 年 9 月 20日'
ms.openlocfilehash: bcbc3d21a03c1585288ad23b1fb2d311d686f55c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570451"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  
> [in]変換するメッセージへのポインター。 **LPMESSAGE**の型定義の mapidefs.h を参照してください。
    
 _pstm_
  
> [out]ストリームを出力する[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスです。 
    
 _ulFlags_
  
>  [in]コンバーターで特定のアクションを示すフラグです。 
    
CCSF_8BITHEADERS
  
> コンバーターは、8 ビットのヘッダーを許可する必要があります。
    
CCSF_EMBEDDED_MESSAGE
  
> 未送信の X で送信された未送信の情報が保持されます。
    
CCSF_GLOBAL_MESSAGE
  
> コンバーターは、国際的なメッセージ (EAI/RFC6530) を構築する必要があります。
    
CCSF_INCLUDE_BCC
  
> MAPI メッセージの BCC 受信者は、MIME ストリームに入れるべきです。
    
CCSF_NO_MSGID
  
> 送信メッセージのメッセージ Id フィールドは含まれません。
    
CCSF_NOHEADERS
  
> コンバーターでは、外部のメッセージのヘッダーを無視してください。
    
CCSF_PLAIN_TEXT_ONLY
  
> コンバーター テキスト形式を送信する必要があります。
    
CCSF_SMTP
  
> コンバーターは、SMTP メッセージが渡されています。 このフラグを設定することが常にする必要があります。
    
CCSF_USE_RTF
  
> コンバーターは、HTML から MIME メッセージ内の RTF 形式に変換する必要があります。
    
CCSF_USE_TNEF
  
> コンバーターでは、MIME メッセージのトランスポート ニュートラル カプセル化形式 (TNEF) 形式を使用します。
    
## <a name="return-values"></a>戻り値

E_INVALIDARG
  
> 無効なフラグが渡された、または*pmsg*または*pstm*では NULL です。 
    
## <a name="remarks"></a>注釈

標準の Outlook メッセージの種類に対してのみサポートされています。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。  <br/> |
   
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


[MAPI �萔](mapi-constants.md)

