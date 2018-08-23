---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a13d4e54900989c692add85add6853a1b511f448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800420"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**適用対象**: Outlook 
  
変換時に使用するエンコーディングを初期化します。
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>パラメーター

_et_
  
> ( [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) ) の値です。 次の値のみがサポートされています。 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>戻り値

E_INVALIDARG
  
> 渡されるエンコードの種類が無効でした。
    
## <a name="remarks"></a>注釈

[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を使用して変換を実行する前に、 **SetEncoding**を呼び出します。 
  
メール アイテムの最も外側のメッセージの本文のみのエンコーディングを設定するのにには、 **SetEncoding**を使用します。 Microsoft Outlook 2010 と Microsoft Outlook 2013 は、個々 の添付ファイルのエンコーディングを選択します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI �萔](mapi-constants.md)

