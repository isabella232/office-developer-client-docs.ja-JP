---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 37850604467384906fec972fd497ae4d9049edcd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610707"
---
# <a name="iconvertersessionsetsaveformat"></a>IConverterSession::SetSaveFormat

**適用対象**: Outlook 2013 | Outlook 2016 
  
コンバーターが [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)で MIME ストリームを返す形式を設定します。
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a>パラメーター

_mstSaveFormat_
  
> [in]MIME ストリームに使用する保存形式。 詳細については、列挙型 [MIMESAVETYPE を参照してください](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx)。
    
  - **SAVE_RFC1521**: 既定の MIME を使用します。      
  - **SAVE_RFC822**: uuencode を使用します。
    
## <a name="return-values"></a>戻り値

S_OK
  
> 呼び出しが正常になされました。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI は MimeToMAPI を使用して EML ファイルを MAPI メッセージに変換します。  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI は MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetEncoding](iconvertersession-setencoding.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI 定数](mapi-constants.md)

