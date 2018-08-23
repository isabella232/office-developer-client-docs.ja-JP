---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f1a4834fc600cc93eeb7fc96563723326c7f2169
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800422"
---
# <a name="iconvertersessionsetsaveformat"></a>IConverterSession::SetSaveFormat

**適用対象**: Outlook 
  
コンバーターが[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)で、MIME ストリームを取得する書式を設定します。
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a>パラメーター

_mstSaveFormat_
  
> [in]保存の MIME ストリームに使用する書式を設定します。 詳細については、 [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx)列挙型を参照してください。
    
  - **SAVE_RFC1521**: 既定値は、MIME を使用します。      
  - **SAVE_RFC822**: でも、uuencode を使用します。
    
## <a name="return-values"></a>戻り値

S_OK
  
> 呼び出しが正常になされました。
    
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
- [IConverterSession::SetEncoding](iconvertersession-setencoding.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI �萔](mapi-constants.md)

