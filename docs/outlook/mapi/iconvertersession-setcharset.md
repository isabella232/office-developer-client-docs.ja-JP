---
title: iconvertersessionsetcharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336660"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi メッセージを mime ストリームに変換するときに mapi から mime コンバータが使用するオプションの文字セットを指定します。
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>パラメーター

 _fapply_
  
> 順番変換に特定の文字セットを使用するかどうかを示します。 このパラメーターを**true**に設定すると、その後の変換で文字セットが適用されます。 特定の文字セットを適用しない場合は、このパラメーターを**false**に設定し、以降のメッセージの既定値に戻します。 
    
 _hcharset_
  
> 順番Windows メールの mimeole で定義されている文字セットへのハンドル。 特定の文字セットを適用しないように指定するには、 **null**を指定します。 **null**以外の値の場合は、 [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx)などの関数を使用して、文字セットのハンドルを取得します。 
    
 _csetapplytype_
  
> 順番Windows メールの mimeole で定義されているように、文字セットを適用してメッセージを変換する方法を指定します。
    
## <a name="return-value"></a>戻り値

S_OK
  
> 関数呼び出しが成功しました。
    
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
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

