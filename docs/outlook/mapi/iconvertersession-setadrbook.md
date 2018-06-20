---
title: IConverterSessionSetAdrBook
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e6880a32e30b8f208ce5ba0a2d30e635ff464461
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800410"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**適用されます**: Outlook 
  
MAPI メッセージを MIME ストリームに変換するときにあいまいなアドレスを解決するのには MIME コンバーターに MAPI を使用して MAPI アドレス帳を指定します。
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parameters

 _個人用アドレス帳_
  
> [in]ポインター、 [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) 、MAPI MIME への変換からに使用するインターフェイスです。 アドレス帳は必要がなくなったとき、このパラメーターを**null**に設定します。これは、インターフェイスを解放し、コンバーターをリセットし、任意のアドレス帳を使用していません。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 関数の呼び出しが成功します。
    
## <a name="remarks"></a>備考

MAPI に変換するメッセージを MIME ストリームを一般的には必要ありません MAPI プロファイルにログオンします。 ただし、変換するための MAPI アドレス帳を指定する場合は、アドレス帳を取得するのにはプロファイルにログオンしている必要があります。
  
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

