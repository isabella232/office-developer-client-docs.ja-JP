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
  
カプセル化されたメッセージのテキストにストリーム インターフェイスを開きます。
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>パラメーター

 _lpMessage_
  
> [in]ストリームが関連付けられているメッセージへのポインター。 このメッセージは、呼び出しで [OpenTnefStream または OpenTnefStreamEx](opentnefstream.md) 関数に渡されるメッセージと同じである [必要](opentnefstreamex.md) はありません。 
    
 _ulFlags_
  
> [in]ストリーム インターフェイスの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_CREATE 
  
> 現在のメッセージにプロパティが存在しない場合は、作成する必要があります。 プロパティが存在する場合は、プロパティ内の現在のデータを、Transport-Neutral カプセル化形式 (TNEF) ストリームのデータに置き換える必要があります。 実装でオブジェクト フラグを設定MAPI_CREATE、実装フラグも設定MAPI_MODIFYがあります。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定のインターフェイスは読み取り専用です。 MAPI_MODIFY設定する場合は常に、MAPI_CREATEする必要があります。
    
 _lppStream_
  
> [out]渡されたカプセル化されたメッセージの **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティのテキストを含み [、IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) インターフェイスをサポートするストリーム オブジェクトへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::OpenTaggedBody** メソッドを呼び出して、カプセル化されたメッセージのテキスト (つまり、TNEF オブジェクト上) のストリーム インターフェイスを開きます。 
  
**OpenTaggedBody** は、処理の一環として、メッセージ テキスト内の添付ファイルまたは OLE オブジェクトの位置を示す添付ファイル タグを挿入または解析します。 添付ファイルタグの形式は次のとおりです。 
  
 **[[**_添付ファイル名_ **:** _添付ファイル_**コンテナー名**] の _n]_ 
  
 _添付ファイル名は_、添付ファイル オブジェクトを表します。 _n_ は、シーケンスの一部である添付ファイルを識別する数値で [、OpenTnefStream](opentnefstream.md)または [OpenTnefStreamEx](opentnefstreamex.md)関数の _lpKey_ パラメーターで渡された値から増分します。添付 _ファイル コンテナー名は_、添付ファイル オブジェクトが存在する物理コンポーネントを表します。 
  
 **OpenTaggedBody は** メッセージ テキストを読み取り、添付ファイル オブジェクトがテキストに最初に表示された場所に添付ファイル タグを挿入します。 元のメッセージ テキストは変更されません。 
  
タグを持つメッセージがストリームに渡される場合、タグは削除され、添付ファイル オブジェクトはストリーム内のタグの位置に移動されます。
  
## <a name="see-also"></a>関連項目



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagBody 標準プロパティ](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

