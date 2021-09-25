---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d05b08cd18b075119017163c7142e88afba82121
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600986"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI から MIME への変換時に、MAPI から MIME への変換であいまいなアドレスを解決するために使用するオプションの MAPI アドレス帳を指定します。
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>パラメーター

 _pab_
  
> [in]MAPI から MIME への変換で使用する [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) インターフェイスへのポインター。 アドレス帳が不要 **になった** 場合は、このパラメーターを null に設定します。これにより、インターフェイスが解放され、コンバータがアドレス帳を使用しなかにリセットされます。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 関数呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

MAPI メッセージを MIME ストリームに変換する場合、通常は MAPI プロファイルにログオンする必要があります。 ただし、変換用に MAPI アドレス帳を指定するには、プロファイルにログオンしてアドレス帳を取得する必要があります。
  
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

