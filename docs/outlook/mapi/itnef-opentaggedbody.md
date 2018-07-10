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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ed433dc1fcf2a366d2ece07ac06d4e12558e4aa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801229"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**適用されます**: Outlook 
  
カプセル化されたメッセージのテキストのストリームのインタ フェースを開きます。
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in]ストリームが関連付けられているメッセージへのポインター。 このメッセージは、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで渡されるのと同じメッセージである必要はありません。 
    
 _ulFlags_
  
> [in]ストリーム インターフェイスを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
タグ 
  
> 現在のメッセージのプロパティがない場合は作成する必要があります。 プロパティが存在する場合、トランスポート ニュートラル カプセル化形式 (TNEF) ストリームからデータをプロパティの現在のデータを交換する必要があります。 実装では、タグのフラグを設定するとき、にも MAPI_MODIFY フラグを設定する必要があります。
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 デフォルトのインタ フェースは、読み取り専用です。 タグを設定するたびに、MAPI_MODIFY を設定する必要があります。
    
 _lppStream_
  
> [out]([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティを渡すには、からのテキストを含んでいるストリーム オブジェクトへのポインターへのポインターがメッセージをカプセル化し、 [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx)インターフェイスをサポートします。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>備考

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイがカプセル化されたメッセージのテキストのストリーム インターフェイスを開くに**ITnef::OpenTaggedBody**メソッドを呼び出します (つまり、TNEF のオブジェクト)。 
  
処理の一環として、 **OpenTaggedBody**は挿入するか、またはメッセージのテキスト内のすべての添付ファイルまたは OLE オブジェクトの位置を示すタグを添付ファイルを解析し。 添付ファイルのタグは、次の形式では。 
  
 **[** **::** の_添付ファイル名_ _n_ **の**_コンテナー名の添付ファイル_ **]**
  
 _添付ファイル名_が添付ファイルのオブジェクトを説明します。 _n_は、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の_lpKey_パラメーターに渡された値からインクリメントするシーケンスの一部である添付ファイルを識別する番号_コンテナー名の添付ファイル_が添付ファイルのオブジェクトが存在する物理コンポーネントを説明しています。 
  
 **OpenTaggedBody**メッセージのテキストを読み込んで、attachment オブジェクトは、テキストで表示されていた元の場所に、添付ファイルのタグを挿入します。 元のメッセージ テキストは変更されません。 
  
タグを持つメッセージは、ストリームとタグを削除した添付ファイルのオブジェクトは、ストリーム内のタグの位置に再配置されます。
  
## <a name="see-also"></a>関連項目



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagBody の標準的なプロパティ](pidtagbody-canonical-property.md)
  
[ITnef: IUnknown](itnefiunknown.md)
