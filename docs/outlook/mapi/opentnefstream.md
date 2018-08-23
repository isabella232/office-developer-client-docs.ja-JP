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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 866d3be5e1c7a4375db84d1f15802e01f8d10f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801696"
---
# <a name="opentnefstream"></a>OpenTnefStream

**適用対象**: Outlook 
  
MAPI トランスポート ニュートラル カプセル化形式 (TNEF) セッションを開始するトランスポート プロバイダーによって呼び出されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |トランスポート プロバイダー  <br/> |
   
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

_lpvSupport_
  
> [in]サポート オブジェクト、または NULL を渡します。 
    
_lpStream_
  
> [in]ソースまたは TNEF ストリーム メッセージの出力先を提供するストレージ ストリーム オブジェクト OLE の**IStream**インターフェイスへのポインター。 
    
_lpszStreamName_
  
> [in]TNEF オブジェクトを使用するデータ ストリームの名前へのポインター。 呼び出し元が**OpenTnefStream**の呼び出しで、TNEF_ENCODE フラグ ( _ulFlags_パラメーター) を設定した場合_lpszName_パラメーター ファイルの名前を付けるために有効とみなされる任意の文字で構成される null 以外の文字列に null 以外のポインターを指定してください。 MAPI は、文字を含む文字列の名前を許可しない"["、"]"、または」:」ファイル ・ システムの使用を許可する場合でも。 _LpszName_に渡される文字列のサイズは、パス名を含む文字列の最大長、MAX_PATH の値を超えていない必要があります。 
    
_ulFlags_
  
> [in]関数のモードを指定するためのフラグのビットマスクです。 次のフラグを設定することができます。
    
TNEF_BEST_DATA 
  
> 使用可能なすべてのプロパティは、その下位レベルの属性にマップされますが、下位レベルの属性への変換により、データ損失の可能性がある場合は、プロパティはエンコードされますが、カプセル化の。 TNEF ストリーム内の情報の重複は、注意してください。 TNEF_BEST_DATA は、他のモードが指定されていない場合のデフォルトです。 
    
TNEF_COMPATIBILITY 
  
> アプリケーションの以前のクライアントとの下位互換性を提供します。 TNEF ストリームがこのフラグを使用してエンコードされたは、使用可能なすべてのプロパティを対応する下位レベルの属性にマップされます。 このモードは、下位レベルのクライアントに必要ないくつかのプロパティの既定値にも発生します。 
    
  > [!CAUTION]
  > このフラグは廃止されて、使用する必要があります。 
  
TNEF_DECODE 
  
> TNEF オブジェクトは指定されたストリームは、読み取り専用アクセスで開かれます。 トランスポート プロバイダーは、それ以降のデコード用のオブジェクトを初期化する関数の場合、このフラグを設定する必要があります。
    
TNEF_ENCODE 
  
> 読み取り/書き込みアクセス許可を指定されたストリームで TNEF オブジェクトが開かれます。 トランスポート プロバイダーは、それ以降をエンコードするためのオブジェクトを初期化する関数の場合、このフラグを設定する必要があります。
    
TNEF_PURE 
  
> MAPI のカプセル化のブロックには、すべてのプロパティをエンコードします。 したがって、TNEF ファイルを「純粋な」では、でほとんどの場合 attMAPIProps attAttachment attRenddata、および attRecipTable。 このモードは、下位互換性を維持する必要がないときに使用に最適です。
    
_lpMessage_
  
> [in]デコードされた添付ファイル付きメッセージの宛先や添付ファイルのエンコードされたメッセージのソースとして、メッセージのオブジェクトへのポインター。 複製先のメッセージのプロパティは、エンコードされたメッセージのプロパティによって上書きされる可能性があります。
    
_wKey_
  
> [in]TNEF オブジェクトを使用して添付ファイルをメッセージのテキストに挿入されたテキストのタグに一致する検索キーです。 この値は、メッセージ間で比較的一意である必要があります。
    
_lppTNEF_
  
> [out]新しい TNEF オブジェクトへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

TNEF オブジェクトが後で、 **OpenTnefStream**関数によって作成された OLE メソッド サポート オブジェクト、ストリーム オブジェクト、およびメッセージのオブジェクトへの参照を追加するのには**IUnknown::AddRef**を呼び出します。 トランスポート プロバイダーは、OLE**が**オブジェクトのメソッド、TNEF を 1 回の呼び出しですべての 3 つのオブジェクトの参照を解放できます。 
  
**OpenTnefStream** TNEF ストリームのメッセージにメッセージの MAPI **IMessage**インターフェイスをエンコードに使用するプロバイダーの TNEF オブジェクトの**ITnef**インターフェイスを初期化します。 代わりに、関数は、MAPI メッセージに TNEF ストリーム メッセージをデコードするのには[ITnef::ExtractProps](itnef-extractprops.md)以降の呼び出しに使用するプロバイダーのオブジェクトを設定できます。 TNEF オブジェクトを解放し、セッションを閉じる、トランスポート プロバイダーはオブジェクトの継承**が**メソッドを呼び出す必要があります。 
  
この関数は、TNEF のアクセスのための元のエントリ ポイントし[OpenTnefStreamEx](opentnefstreamex.md)によって置き換えられましたが、既に TNEF を使用するために互換性のために使用されます。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

