---
title: IConverterSessionSetCharSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b951eeb555f800d1e625e68806ba6b19352410b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616832"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI メッセージを MIME ストリームに変換するときに MAPI から MIME コンバータに使用するオプションの文字セットを指定します。
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>パラメーター

 _fApply_
  
> [in]変換に特定の文字セットを使用するかどうかを示します。 以降の変換で **文字セットを** 適用するには、このパラメーターを true に設定します。 特定の **文字セットを** 適用し、後続のメッセージの既定値に戻す場合は、このパラメーターを false に設定します。 
    
 _hcharset_
  
> [in]mail の mimeole.h で定義されている文字セットWindows。 特定 **の文字** セットを適用しない場合は null を指定します。 null 以外の **値の** 場合は [、MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) などの関数を使用して、文字セットのハンドルを取得します。 
    
 _csetapplytype_
  
> [in]mail の mimeole.h で定義されているメッセージを変換する文字セットを適用するWindowsします。
    
## <a name="return-value"></a>戻り値

S_OK
  
> 関数呼び出しが成功しました。
    
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
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

