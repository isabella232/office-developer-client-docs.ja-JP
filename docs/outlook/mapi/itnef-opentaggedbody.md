---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348735"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
カプセル化されたメッセージのテキストにストリームインターフェイスを開きます。
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>パラメーター

 _lpmessage_
  
> 順番stream が関連付けられているメッセージへのポインター。 このメッセージは、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで渡されるメッセージと同じである必要はありません。 
    
 _ulFlags_
  
> 順番stream インターフェイスを開く方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_CREATE 
  
> プロパティが現在のメッセージ内に存在しない場合は、作成する必要があります。 プロパティが存在する場合、プロパティの現在のデータは、トランスポートに中立的なカプセル化形式 (TNEF) ストリームのデータに置き換える必要があります。 実装で MAPI_CREATE フラグが設定されている場合は、MAPI_MODIFY フラグも設定する必要があります。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定のインターフェイスは読み取り専用です。 MAPI_CREATE が設定されている場合は常に、MAPI_MODIFY を設定する必要があります。
    
 _lppstream_
  
> 読み上げ渡されたカプセル化されたメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティから、 [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)インターフェイスをサポートするテキストを含む stream オブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>解説

トランスポートプロバイダー、メッセージストアプロバイダー、およびゲートウェイは、 **ITnef:: OpenTaggedBody**メソッドを呼び出して、カプセル化されたメッセージ (つまり TNEF オブジェクト) のテキストのストリームインターフェイスを開きます。 
  
**OpenTaggedBody**は、処理の一環として、メッセージテキスト内の添付ファイルまたは OLE オブジェクトの位置を示す添付ファイルタグを挿入または解析します。 添付ファイルタグは、次の形式になります。 
  
 **[[** 添付ファイル_名_ **:** _n_ **** _添付ファイルコンテナー名_ **]]**
  
 _添付ファイル名_添付ファイルオブジェクトについて説明します。 _n_は、シーケンスの一部である添付ファイルを識別する数値で、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の_lpkey_パラメーターで渡された値を増分します。_添付ファイルコンテナー名_は、attachment オブジェクトが存在する物理コンポーネントを表します。 
  
 **OpenTaggedBody**は、メッセージテキストを読み取り、添付ファイルオブジェクトが最初にテキストに表示された場所に添付ファイルのタグを挿入します。 元のメッセージテキストは変更されません。 
  
タグを持つメッセージが stream に渡されると、タグが削除され、添付ファイルオブジェクトがストリーム内のタグの位置に移動されます。
  
## <a name="see-also"></a>関連項目



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagBody 標準プロパティ](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

