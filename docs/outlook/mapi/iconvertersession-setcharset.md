---
title: IConverterSessionSetCharSet
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
ms.openlocfilehash: 69023d2c13037fb52a4d1dc4f7376efbd839aebc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581700"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
オプションの文字セットを MAPI MIME コンバーターの使用する MAPI メッセージを MIME ストリームに変換するときを指定します。
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>パラメーター

 _fApply_
  
> [in]特定の文字セット変換を使用するかどうかを示します。 **真**以降の変換中の文字セットを適用するには、このパラメーターを設定します。 任意の特定の文字セットを適用し、後続のメッセージの既定値に戻す必要がなくなった場合は、 **false を指定**するこのパラメーターを設定します。 
    
 _hcharset_
  
> [in]Windows メールの mimeole.h で定義されているように設定する文字へのハンドル。 指定**null**を任意の特定の文字セットを適用しないことを指定します。 非**null**値は、文字セットへのハンドルを取得するのには[MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx)のような関数を使用します。 
    
 _csetapplytype_
  
> [in]Windows メールの mimeole.h で定義されている、メッセージの変換を設定する文字を適用する方法を示します。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 関数の呼び出しが成功します。
    
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
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

