---
title: iconvertersessionsetadrbook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429195"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi メッセージを mime ストリームに変換するときに、あいまいなアドレスを解決するために mapi から mime コンバータが使用するオプションの mapi アドレス帳を指定します。
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>パラメーター

 _個人_
  
> 順番MAPI から MIME への変換で使用される[IAddrBook: imapiprop](iaddrbookimapiprop.md)インターフェイスへのポインター。 アドレス帳を必要としなくなった場合は、このパラメーターを**null**に設定します。これにより、インターフェイスが解放され、すべてのアドレス帳を使用しないようにコンバータがリセットされます。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 関数呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

mapi メッセージを MIME ストリームに変換する必要はありません。通常、mapi プロファイルにログオンする必要はありません。 ただし、変換に MAPI アドレス帳を指定するには、アドレス帳を取得するためにプロファイルにログオンする必要があります。
  
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

