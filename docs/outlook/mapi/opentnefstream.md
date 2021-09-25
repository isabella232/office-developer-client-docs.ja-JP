---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bcda2b9445fca40ba2f67e25b3d6ae7a949ceb52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571382"
---
# <a name="opentnefstream"></a>OpenTnefStream

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI トランスポート ニュートラル カプセル化形式 (TNEF) セッションを開始するためにトランスポート プロバイダーによって呼び出されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |トランスポート プロバイダー  <br/> |
   
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
  
> [in]サポート オブジェクトを渡す、または NULL で渡します。 
    
_lpStream_
  
> [in]TNEF ストリーム メッセージの送信元または宛先を提供する記憶域ストリーム オブジェクト OLE **IStream** インターフェイスへのポインター。 
    
_lpszStreamName_
  
> [in]TNEF オブジェクトが使用するデータ ストリームの名前へのポインター。 呼び出し元が **OpenTnefStream** への呼び出しで TNEF_ENCODE フラグ ( _ulFlags_ パラメーター) を設定している場合 _、lpszName_ パラメーターは、ファイルの命名に有効と見なされる文字で構成される null 以外の文字列への null 以外のポインターを指定する必要があります。 MAPI では、ファイル システムで使用が許可されている場合でも、"[","]"、または ":"という文字を含む文字列名は許可しません。 _lpszName_ に渡される文字列のサイズは、パス名を含む文字列の最大長である MAX_PATH の値を超えないようにしてください。 
    
_ulFlags_
  
> [in]関数のモードを示すために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_BEST_DATA 
  
> 考えられるすべてのプロパティは、ダウンレベルの属性にマップされますが、ダウンレベル属性への変換によってデータが失われる可能性がある場合は、カプセル化でもプロパティがエンコードされます。 これにより、TNEF ストリーム内の情報が重複する可能性があります。 TNEF_BEST_DATAモードが指定されていない場合は、既定値を指定します。 
    
TNEF_COMPATIBILITY 
  
> 古いクライアント アプリケーションとの下位互換性を提供します。 このフラグでエンコードされた TNEF ストリームは、可能なすべてのプロパティを対応するダウンレベル属性にマップします。 また、このモードでは、ダウンレベル のクライアントに必要な一部のプロパティの既定値も発生します。 
    
  > [!CAUTION]
  > このフラグは廃止され、使用できません。 
  
TNEF_DECODE 
  
> 指定されたストリームの TNEF オブジェクトは、読み取り専用アクセスで開きます。 トランスポート プロバイダーは、関数が後続のデコードのためにオブジェクトを初期化する場合は、このフラグを設定する必要があります。
    
TNEF_ENCODE 
  
> 指定されたストリームの TNEF オブジェクトは、読み取り/書き込みアクセス許可のために開きます。 トランスポート プロバイダーは、関数が後続のエンコード用にオブジェクトを初期化する場合は、このフラグを設定する必要があります。
    
TNEF_PURE 
  
> すべてのプロパティを MAPI カプセル化ブロックにエンコードします。 したがって、"純粋な" TNEF ファイルは、多くの場合、attMAPIProps、attAttachment、attRenddata、および attRecipTable で構成されます。 このモードは、下位互換性が必要ない場合に使用する場合に最適です。
    
_lpMessage_
  
> [in]添付ファイルを含むデコードされたメッセージの宛先として、または添付ファイルを含むエンコードされたメッセージのソースとしてメッセージ オブジェクトへのポインター。 宛先メッセージのプロパティは、エンコードされたメッセージのプロパティによって上書きされる可能性があります。
    
_wKey_
  
> [in]TNEF オブジェクトがメッセージ テキストに挿入されたテキスト タグに添付ファイルを一致するために使用する検索キー。 この値は、メッセージ間で比較的一意である必要があります。
    
_lppTNEF_
  
> [out]新しい TNEF オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

**OpenTnefStream** 関数によって作成された TNEF オブジェクトは、後で OLE メソッド **IUnknown::AddRef** を呼び出して、サポート オブジェクト、ストリーム オブジェクト、およびメッセージ オブジェクトの参照を追加します。 トランスポート プロバイダーは、TNEF オブジェクトの OLE メソッド **IUnknown::Release** を 1 回呼び出して、3 つすべてのオブジェクトの参照を解放できます。 
  
**OpenTnefStream** は、プロバイダーが MAPI メッセージ **IMessage** インターフェイスを TNEF ストリーム メッセージにエンコードする場合に使用する TNEF オブジェクト **ITnef** インターフェイスを割り当て、初期化します。 または、この関数は、プロバイダーが [ITnef::ExtractProps](itnef-extractprops.md) への後続の呼び出しで使用するオブジェクトをセットアップして、TNEF ストリーム メッセージを MAPI メッセージにデコードできます。 TNEF オブジェクトを解放し、セッションを閉じるには、トランスポート プロバイダーはオブジェクトの継承 **された IUnknown::Release** メソッドを呼び出す必要があります。 
  
この関数は TNEF アクセスの元のエントリ ポイントであり [、OpenTnefStreamEx](opentnefstreamex.md) に置き換えられたが、TNEF を既に使用しているユーザーの互換性のために使用されます。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

