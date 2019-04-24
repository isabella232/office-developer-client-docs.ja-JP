---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348574"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート、ゲートウェイ、およびメッセージストアで使用するために、tnef データストリームにメッセージオブジェクトをエンコードまたはデコードするために使用できるトランスポート中立カプセル化形式 (TNEF) オブジェクトを作成します。 これは、TNEF アクセスのエントリポイントです。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |トランスポートプロバイダー  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>パラメーター

_lpvsupport_
  
> 順番サポートオブジェクトを渡すか、または NULL を渡します。 null の場合、 _lpAddressBook_パラメーターは null 以外である必要があります。 
    
_lpstream_
  
> 順番TNEF ストリームメッセージのソースまたは送信先を提供する、OLE **IStream**インターフェイスなどのストレージストリームオブジェクトへのポインター。 
    
_lpszstreamname_
  
> 順番TNEF オブジェクトが使用するデータストリームの名前へのポインター。 呼び出し元が**OpenTnefStream**の呼び出しで TNEF_ENCODE フラグ ( _ulflags_パラメーター) を設定している場合、 _lpszname_パラメーターには、null 以外の文字列へのポインターを指定する必要があります。 null 以外の文字には、ファイルの名前付けに対して有効になっていると見なされます。 MAPI では、ファイルシステムで使用が許可されている場合でも、文字 "["、"]"、または ":" を含む文字列名を使用できません。 _lpszname_パラメーターに渡される文字列のサイズは、パス名を含む文字列の最大長である MAX_PATH の値を超えることはできません。 
    
_ulFlags_
  
> 順番関数のモードを示すために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_BEST_DATA 
  
> 可能なすべてのプロパティは、下位レベルの属性にマップされますが、下位レベルの属性への変換によってデータが失われる可能性がある場合、プロパティも encapsulations でエンコードされます。 これにより、TNEF ストリーム内の情報が重複することに注意してください。 他のモードが指定されていない場合の既定値は TNEF_BEST_DATA です。 
    
TNEF_COMPATIBILITY 
  
> 以前のクライアントアプリケーションとの下位互換性を提供します。 このフラグでエンコードされた TNEF ストリームは、使用可能なすべてのプロパティを対応する下位レベルの属性にマップします。 このモードでは、ダウンレベルクライアントに必要な一部のプロパティの既定のプロパティも発生します。 
    
  > [!CAUTION]
  > このフラグは現在使われていないため、使用しないでください。 
  
TNEF_DECODE 
  
> 指定した stream の TNEF オブジェクトは、読み取り専用アクセスで開かれます。 関数がその後のデコードのためにオブジェクトを初期化する場合は、トランスポートプロバイダーがこのフラグを設定する必要があります。
    
TNEF_ENCODE 
  
> 指定した stream の TNEF オブジェクトは、読み取り/書き込みアクセス許可で開かれます。 この関数が後でエンコードするためにオブジェクトを初期化する場合は、トランスポートプロバイダーがこのフラグを設定する必要があります。
    
TNEF_PURE 
  
> すべてのプロパティを MAPI カプセル化ブロックにエンコードします。 そのため、"pure" TNEF ファイルは、ほとんどの場合、属性 attMAPIProps、attRenddata、および attRecipTable で構成されます。 このモードは、下位互換性が必要ない場合に使用するのに適しています。
    
_lpmessage_
  
> 順番添付ファイル付きのデコードされたメッセージの送信先としてのメッセージオブジェクトへのポインター、および添付ファイル付きのエンコードされたメッセージのソース。 転送先メッセージのすべてのプロパティは、エンコードされたメッセージのプロパティによって上書きできます。
    
_wKeyVal_
  
> 順番TNEF オブジェクトは、メッセージテキストに挿入されたテキストタグに添付ファイルを照合するために使用する検索キーです。 この値は、メッセージ間で比較的一意である必要があります。 
    
_lpAddressBook_
  
> 順番エントリ id のアドレス指定情報を取得するために使用されるアドレス帳オブジェクトへのポインター。 
    
_lpptnef_
  
> 読み上げ新しい TNEF オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

**OpenTnefStreamEx**関数は、 [OpenTnefStream](opentnefstream.md)に推奨される代替の方法であり、TNEF アクセスの元のエントリポイントです。 
  
後で**OpenTnefStreamEx**関数によって作成された TNEF オブジェクトは、OLE メソッド**IUnknown:: AddRef**を呼び出して、support オブジェクト、stream オブジェクト、および message オブジェクトへの参照を追加します。 トランスポートプロバイダーは、TNEF オブジェクトの OLE メソッド**IUnknown:: release**に対して1回の呼び出しで、3つのすべてのオブジェクトの参照を解放できます。 
  
**OpenTnefStreamEx**は、プロバイダーが tnef オブジェクトを割り当てて初期化し、それを使用して、tnef ストリームメッセージへの MAPI メッセージのエンコードに使用します。 別の方法として、この関数はプロバイダーのオブジェクトを設定して、 [ITnef:: ExtractProps](itnef-extractprops.md)への以降の呼び出しで、TNEF ストリームメッセージを MAPI メッセージにデコードすることもできます。 TNEF オブジェクトを解放してセッションを閉じるには、トランスポートプロバイダーは、オブジェクトに対して継承された**IUnknown:: Release**メソッドを呼び出す必要があります。 
  
_wKeyVal_パラメーターの基本値を0にすることはできません。また、 **OpenTnefStreamEx**のすべての呼び出しで同じにすることはできません。 代わりに、ランタイムライブラリの乱数ジェネレーターから、システム時間に基づいてランダムな番号を使用します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ファイル .cpp  <br/> |LoadFromTNEF  <br/> |mfcmapi は、 **OpenTnefStreamEx**メソッドを使用して TNEF ファイルのストリームを開くため、プロパティが抽出される可能性があります。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

