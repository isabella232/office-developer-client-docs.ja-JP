---
title: iconvertersessionsetencoding
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
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341301"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**適用対象**: Outlook 2013 | Outlook 2016 
  
変換時に使用されるエンコードを初期化します。
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>パラメーター

_et_
  
> [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx)値。 次の値のみがサポートされています。 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>戻り値

E_INVALIDARG
  
> 渡されたエンコードの種類が無効です。
    
## <a name="remarks"></a>解説

[iconvertersession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を使用して変換を実行する前に、 **setencoding**を呼び出します。 
  
**setencoding**を使用して、メールアイテムの最も外側のメッセージ本文にのみエンコードを設定します。 microsoft outlook 2010 および microsoft outlook 2013 各添付ファイルのエンコード方法を選択します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|mapimime .cpp  <br/> |ImportEMLToIMessage  <br/> |mfcmapi は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。  <br/> |
|mapimime .cpp  <br/> |ExportIMessageToEML  <br/> |mfcmapi は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI 定数](mapi-constants.md)

