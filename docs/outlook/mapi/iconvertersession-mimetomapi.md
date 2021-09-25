---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: '最終更新日: 2019 年 9 月 6 日'
ms.openlocfilehash: a24c3cfacaf86369fd5229e9a8beb3dec13d589f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616846"
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
  
> [in] [MIME ストリームへの IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイス。 
    
 _pmsg_
  
> [in]読み込むメッセージへのポインター。 呼び出し元は API に入力するメッセージを指定する必要があります。そのため、オブジェクトは [in] に移動する必要があります。 LPMESSAGE の型定義については、mapidefs.h **を参照してください**。
    
 _pszSrcSrv_
  
> [in]この値は null である **必要があります**。
    
 _ulFlags_
  
> [in]このパラメーターは、変換中に実行される特別なアクションを識別します。 特定のアクションを実行する必要がない場合、または次の値の組み合わせを 0 に設定する必要があります。
    
CCSF_EMBEDDED_MESSAGE
  
> 送信/送信されていない情報は X-Unsent に保持されます。
    
CCSF_SMTP
  
> MIME ストリームは、簡易メール転送プロトコル (SMTP) メッセージ用です。
    
CCSF_INCLUDE_BCC
  
> MIME ストリームの BCC 受信者は、MAPI メッセージに含める必要があります。
    
CCSF_USE_RTF
  
> MIME ストリームの HTML 本文は、MAPI メッセージでリッチ テキスト形式 (RTF) に変換する必要があります。

CCSF_GLOBAL_MESSAGE
> コンバーターは、MIME ストリームを国際メッセージ (EAI/RFC6530) として処理する必要があります。 2013 年Outlookサポートされていません。
    
## <a name="return-value"></a>戻り値

E_INVALIDARG
  
> _pstm_ が null、pmsg が _null、_ または _ulFlags が無効かどうかを_ 示します。  
    
## <a name="remarks"></a>注釈

_ulFlags_ の **CCSF_USE_RTF** を指定し、宛先メッセージ ストアが HTML と RTF の両方をサポートしている場合、MAPI メッセージは HTML または RTF に変換されます。 メッセージが RTF に変換された場合、変換された形式は RTF 圧縮され、HTML は圧縮された RTF 文字列に埋め込まれます。文字列は [PidTagRtfCompressed Canonical プロパティ](pidtagrtfcompressed-canonical-property.md)に含まれます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI は MimeToMAPI を使用して EML ファイルを MAPI メッセージに変換します。  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI は MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[MAPI 定数](mapi-constants.md)

