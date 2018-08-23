---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f6afa890f61bb2f394e3cf69e0f2c54699a2ad9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803801"
---
# <a name="rtfsync"></a>RTFSync

**適用対象**: Outlook 
  
リッチ テキスト形式 (RTF) メッセージのテキストがテキスト形式のバージョンと一致していることを確認します。 RTF 形式を読み取る前に、RTF 形式を変更した後にこの関数を呼び出す必要があります。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |Rtf 形式に対応したクライアント アプリケーション、およびメッセージ ストア プロバイダー  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>パラメーター

_lpMessage_
  
> [in]更新するメッセージへのポインター。
    
_ulFlags_
  
> [in]Rtf 形式またはテキスト形式のメッセージを示すために使用するフラグのビットが変更されています。 次のフラグを設定することができます。
    
  - RTF_SYNC_BODY_CHANGED: メッセージのテキスト形式のバージョンが変更されました。
      
  - RTF_SYNC_RTF_CHANGED: RTF 形式のメッセージが変更されました。
    
  _UlFlags_パラメーターで他のすべてのビットは、将来使用するために予約されています。 
    
_lpfMessageUpdated_
  
> [out]更新されたメッセージが表示されるかどうかを示す変数へのポインター。 TRUE を指定するとメッセージが表示される更新された、FALSE それ以外の場合。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) のプロパティが存在しないか、FALSE が使用され、RTF_SYNC_BODY_ のプロパティを読み取って、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))**へ**の関数を呼び出す必要があります前にフラグが設定を変更します。 
  
**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティでは、STORE_RTF_OK フラグは設定されていない場合、RTF_SYNC_RTF_CHANGED フラグが設定されている**PR_RTF_COMPRESSED**を変更した後でこの関数が呼び出さ 必要があります。 
  
([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**と**PR_RTF_COMPRESSED**の両方が変更されている場合両方のフラグが設定を**行う**関数を呼び出す必要があります。 
  
_LpfMessageUpdated_パラメーターの値は、TRUE に設定されている場合、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要があります。 **SaveChanges**が呼び出されない場合、メッセージの変更は保存されません。 
  
メッセージ ストア プロバイダーは、 **PR_BODY**と**PR_RTF_COMPRESSED**プロパティの同期を維持するのに、**行う**を使用できます。 
  
詳細については、[メッセージ ストア プロバイダーの rtf 形式のテキストをサポートしている](supporting-rtf-text-for-message-store-providers.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)

