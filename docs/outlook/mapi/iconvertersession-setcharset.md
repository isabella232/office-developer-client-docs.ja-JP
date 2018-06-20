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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 032f071e18af3a89a2850cf2bd1e141f34bc86d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800415"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**適用されます**: Outlook 
  
オプションの文字セットを MAPI MIME コンバーターの使用する MAPI メッセージを MIME ストリームに変換するときを指定します。
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parameters

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



[IConverterSession: IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

