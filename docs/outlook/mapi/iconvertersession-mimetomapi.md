---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: '最終更新日: 2019 年9月6日'
ms.openlocfilehash: f6f671cbfd5e14d602aaa31d31e54e859f068593
ms.sourcegitcommit: 27a9f3568318470e7ee09ad93a90c3f80d3ef0cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2019
ms.locfileid: "36790772"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MIME ストリームを MAPI メッセージに変換します。
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>パラメーター

 _pstm_
  
> 順番MIME ストリームへの[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイス。 
    
 _pmsg_
  
> 順番読み込むメッセージへのポインター。 呼び出し元は、API に入力するメッセージを指定する必要があるので、オブジェクトを [in] に設定する必要があります。 **Lpmessage**の種類の定義については、「mapidefs.h」を参照してください。
    
 _pszSrcSrv_
  
> 順番この値は**null**である必要があります。
    
 _ulFlags_
  
> 順番このパラメーターには、変換中に実行する特別なアクションを指定します。 特定のアクションを実行する必要がない場合、または次の値の組み合わせを指定する場合は、ゼロ (0) である必要があります。
    
CCSF_EMBEDDED_MESSAGE
  
> 送信/未送信の情報は、X 未送信の情報として保持されます。
    
CCSF_SMTP
  
> MIME ストリームは、簡易 MAPI 転送プロトコル (SMTP) メッセージのためのものです。
    
CCSF_INCLUDE_BCC
  
> MIME ストリームの BCC 受信者は、MAPI メッセージに含める必要があります。
    
CCSF_USE_RTF
  
> MIME ストリームの HTML 本文は、MAPI メッセージでリッチテキスト形式 (RTF) に変換する必要があります。

CCSF_GLOBAL_MESSAGE
> コンバータは、MIME ストリームを国際メッセージ (EAI/RFC6530) として処理する必要があります。 Outlook 2013 ではサポートされていません。
    
## <a name="return-value"></a>戻り値

E_INVALIDARG
  
> _Pstm_が**null**、 _Pmsg_が**null**、 _ulflags_が無効であることを示します。 
    
## <a name="remarks"></a>解説

**CCSF_USE_RTF**を_ulflags_の一部として指定して、宛先メッセージストアが html と rtf の両方をサポートしている場合、MAPI メッセージは html または rtf に変換されます。 メッセージが RTF に変換される場合、変換された形式は RTF 形式に変換され、すべての HTML が圧縮 RTF 文字列に埋め込まれ、文字列が[PidTagRtfCompressed 標準プロパティ](pidtagrtfcompressed-canonical-property.md)に格納されます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MapiMime .cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。  <br/> |
|MapiMime .cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[MAPI 定数](mapi-constants.md)

