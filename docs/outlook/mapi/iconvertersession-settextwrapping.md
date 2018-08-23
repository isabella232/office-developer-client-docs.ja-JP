---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a89f6dd14e8bbea9d0d4145dc05bf332af95234a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573635"
---
# <a name="iconvertersessionsettextwrapping"></a>IConverterSession::SetTextWrapping

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テキストの折り返しのコンバーターから[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)で返される MIME ストリームの幅を設定します。
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a>パラメーター

 *fWrapText* 
  
> [in]テキストを折り返すかどうかどうか。
    
 *ulWrapWidth* 
  
> [in]テキストの折り返しの幅を使用します。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 呼び出しが正常になされました。
    
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)


[MAPI �萔](mapi-constants.md)

