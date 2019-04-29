---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423959"
---
# <a name="opentnefstream"></a>OpenTnefStream

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI トランスポートのニュートラルカプセル化形式 (TNEF) セッションを開始するために、トランスポートプロバイダーによって呼び出されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |トランスポートプロバイダー  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>パラメーター

_lpvsupport_
  
> 順番サポートオブジェクトを渡すか、または NULL を渡します。 
    
_lpstream_
  
> 順番TNEF ストリームメッセージのソースまたは送信先を提供する、ストレージストリームオブジェクトの OLE **IStream**インターフェイスへのポインター。 
    
_lpszstreamname_
  
> 順番TNEF オブジェクトが使用するデータストリームの名前へのポインター。 呼び出し元が**OpenTnefStream**の呼び出しで TNEF_ENCODE フラグ ( _ulflags_パラメーター) を設定している場合、 _lpszname_パラメーターには、null 以外の文字列へのポインターを指定する必要があります。 null 以外の文字には、ファイルの名前付けに対して有効になっていると見なされます。 MAPI では、ファイルシステムで使用が許可されている場合でも、文字 "["、"]"、または ":" を含む文字列名を使用できません。 _lpszname_に渡される文字列のサイズは、パス名を含む文字列の最大長である MAX_PATH の値を超えることはできません。 
    
_ulFlags_
  
> 順番関数のモードを示すために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_BEST_DATA 
  
> 可能なすべてのプロパティは、下位レベルの属性にマップされますが、下位レベルの属性への変換によってデータが失われる可能性がある場合、プロパティも encapsulations でエンコードされます。 これにより、TNEF ストリーム内の情報が重複することに注意してください。 他のモードが指定されていない場合の既定値は TNEF_BEST_DATA です。 
    
TNEF_COMPATIBILITY 
  
> 以前のクライアントアプリケーションとの下位互換性を提供します。 このフラグでエンコードされた TNEF ストリームは、使用可能なすべてのプロパティを対応する下位レベルの属性にマップします。 このモードでは、ダウンレベルクライアントに必要な一部のプロパティの既定のプロパティも発生します。 
    
  > [!CAUTION]
  > このフラグは現在使われていないため、使用しないでください。 
  
TNEF_DECODE 
  
> 指定した stream の TNEF オブジェクトは、読み取り専用アクセスで開かれます。 トランスポートプロバイダーは、このフラグを設定して、関数がオブジェクトを初期化して以降のデコードを行う必要があります。
    
TNEF_ENCODE 
  
> 指定した stream の TNEF オブジェクトは、読み取り/書き込みアクセス許可で開かれます。 このフラグを設定する必要がある場合は、トランスポートプロバイダーは、オブジェクトを初期化して後続のエンコーディングを行う必要があります。
    
TNEF_PURE 
  
> すべてのプロパティを MAPI カプセル化ブロックにエンコードします。 そのため、"純粋な" TNEF ファイルは、最大で、attMAPIProps、/添付ファイル、attRenddata、および attRecipTable で構成されます。 このモードは、下位互換性が必要ない場合に使用するのに適しています。
    
_lpmessage_
  
> 順番添付ファイル付きのデコードされたメッセージの送信先としてのメッセージオブジェクトへのポインター、および添付ファイル付きのエンコードされたメッセージのソース。 転送先メッセージのすべてのプロパティは、エンコードされたメッセージのプロパティによって上書きされる場合があります。
    
_wkey_
  
> 順番TNEF オブジェクトは、メッセージテキストに挿入されたテキストタグに添付ファイルを照合するために使用する検索キーです。 この値は、メッセージ間で比較的一意である必要があります。
    
_lpptnef_
  
> 読み上げ新しい TNEF オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

後で**OpenTnefStream**関数によって作成された TNEF オブジェクトは、OLE メソッド**IUnknown:: AddRef**を呼び出して、support オブジェクト、stream オブジェクト、および message オブジェクトへの参照を追加します。 トランスポートプロバイダーは、TNEF オブジェクトの OLE メソッド**IUnknown:: release**に対して1回の呼び出しで、3つのすべてのオブジェクトの参照を解放できます。 
  
**OpenTnefStream**は、MAPI メッセージ**IMessage**インターフェイスを tnef ストリームメッセージにエンコードする際に使用するために、プロバイダー用の tnef オブジェクト**ITnef**インターフェイスを割り当てて初期化します。 または、この関数は、プロバイダーが[ITnef:: ExtractProps](itnef-extractprops.md)への以降の呼び出しで使用するオブジェクトを設定して、TNEF ストリームメッセージを MAPI メッセージにデコードすることもできます。 TNEF オブジェクトを解放してセッションを閉じるには、トランスポートプロバイダーは、オブジェクトに対して継承された**IUnknown:: Release**メソッドを呼び出す必要があります。 
  
この関数は、tnef アクセスの元のエントリポイントであり、 [OpenTnefStreamEx](opentnefstreamex.md)に置き換えられていますが、既に tnef を使用している場合の互換性のためにも使用されています。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

