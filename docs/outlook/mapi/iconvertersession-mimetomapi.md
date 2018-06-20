---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 03a67371c67d5f0ac346470ec7ab38bb67d5ce2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800408"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**適用されます**: Outlook 
  
MIME ストリームを MAPI メッセージに変換します。
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameters

 _pstm_
  
> [in]MIME ストリームの[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスです。 
    
 _pmsg_
  
> [out]ロードするのには、メッセージへのポインター。 **LPMESSAGE**の型定義の mapidefs.h を参照してください。
    
 _pszSrcSrv_
  
> [in]この値を**null**にする必要があります。
    
 _ulFlags_
  
> [in]このパラメーターは、変換中に実行される特別な操作を識別します。 ゼロ (0) を実行するには、特定のアクションがない場合、または次の値の組み合わせである必要があります。
    
CCSF_EMBEDDED_MESSAGE
  
> 未送信の X で送信された未送信の情報が保持されます。
    
CCSF_SMTP
  
> MIME ストリームでは、簡易 MAPI 転送プロトコル (SMTP) メッセージです。
    
CCSF_INCLUDE_BCC
  
> MIME ストリームの BCC 受信者が MAPI メッセージに含まれます。
    
CCSF_USE_RTF
  
> MAPI メッセージの MIME ストリームの HTML 本文をリッチ テキスト形式 (RTF) に変換する必要があります。
    
## <a name="return-value"></a>�߂�l

E_INVALIDARG
  
> _Pstm_が**null**こと、 _pmsg_が**null**、または、 _ulFlags_が有効ではありませんを示します。 
    
## <a name="remarks"></a>備考

_UlFlags_の一部として**CCSF_USE_RTF**を指定した送信先メッセージ ・ ストアが HTML や rtf 形式の両方をサポートしている場合は、MAPI メッセージは、html 形式または rtf 形式に変換されます。 変換後のフォーマットを圧縮する場合は、メッセージを rtf 形式に変換すると、rtf 形式、HTML は、圧縮された RTF 文字列に埋め込まれ、 [PidTagRtfCompressed の標準的なプロパティ](pidtagrtfcompressed-canonical-property.md)に文字列が含まれます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IConverterSession: IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[MAPI �萔](mapi-constants.md)

