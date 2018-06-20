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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 52fd844954f41d5d09b5e78f7c23ff6f7469bb43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801704"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**適用されます**: Outlook 
  
エンコードまたは TNEF データ ストリームを使用するメッセージ オブジェクトをデコードするトランスポートまたはゲートウェイとメッセージ ストアで使用できるトランスポート ニュートラル カプセル化形式 (TNEF) オブジェクトを作成します。 これは、TNEF のアクセスのエントリ ポイントです。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |トランスポート プロバイダー  <br/> |
   
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

## <a name="parameters"></a>Parameters

_lpvSupport_
  
> [in]サポート オブジェクト、または NULL を渡します。 NULL の場合、 _lpAddressBook_パラメーターは、null のはずです。 
    
_lpStream_
  
> [in]ソースまたは TNEF ストリーム メッセージの出力先を提供する、OLE の**IStream**インターフェイスなど、ストレージのストリーム オブジェクトへのポインター。 
    
_lpszStreamName_
  
> [in]TNEF オブジェクトを使用するデータ ストリームの名前へのポインター。 呼び出し元が**OpenTnefStream**の呼び出しで、TNEF_ENCODE フラグ ( _ulFlags_パラメーター) を設定した場合_lpszName_パラメーター ファイルの名前を付けるために有効とみなされる任意の文字で構成される null 以外の文字列に null 以外のポインターを指定してください。 MAPI は、文字を含む文字列の名前を許可しない"["、"]"、または」:」ファイル ・ システムの使用を許可する場合でも。 _LpszName_パラメーターに渡される文字列のサイズは、パス名を含む文字列の最大長、MAX_PATH の値を超えていない必要があります。 
    
_ulFlags_
  
> [in]関数のモードを指定するためのフラグのビットマスクです。 次のフラグを設定することができます。
    
TNEF_BEST_DATA 
  
> 使用可能なすべてのプロパティは、その下位レベルの属性にマップされますが、下位レベルの属性への変換により、データ損失の可能性がある場合は、プロパティはエンコードされますが、カプセル化の。 TNEF ストリーム内の情報の重複は、注意してください。 TNEF_BEST_DATA は、他のモードが指定されていない場合のデフォルトです。 
    
TNEF_COMPATIBILITY 
  
> 古いバージョンのクライアント アプリケーションとの下位互換性を提供します。 TNEF ストリームがこのフラグを使用してエンコードされたは、使用可能なすべてのプロパティを対応する下位レベルの属性にマップされます。 このモードは、下位レベルのクライアントに必要ないくつかのプロパティの既定値にも発生します。 
    
  > [!CAUTION]
  > このフラグは廃止されて、使用する必要があります。 
  
TNEF_DECODE 
  
> TNEF オブジェクトは指定されたストリームは、読み取り専用アクセスで開かれます。 トランスポート プロバイダーは、機能は、それ以降のデコード用のオブジェクトを初期化する場合、このフラグを設定する必要があります。
    
TNEF_ENCODE 
  
> 読み取り/書き込みアクセス許可を指定されたストリームで TNEF オブジェクトが開かれます。 トランスポート プロバイダーは、機能は、それ以降をエンコードするためのオブジェクトを初期化する場合、このフラグを設定する必要があります。
    
TNEF_PURE 
  
> MAPI のカプセル化のブロックには、すべてのプロパティをエンコードします。 したがって、TNEF ファイルを「純粋な」では、多くて属性の attMAPIProps attAttachment attRenddata、および attRecipTable。 このモードは、下位互換性を維持する必要がないときに使用に最適です。
    
_lpMessage_
  
> [in]デコードされた添付ファイル付きメッセージの宛先や添付ファイルのエンコードされたメッセージのソースとして、メッセージのオブジェクトへのポインター。 エンコードされたメッセージのプロパティでは、複製先のメッセージのプロパティを上書きできます。
    
_wKeyVal_
  
> [in]TNEF オブジェクトを使用して添付ファイルをメッセージのテキストに挿入されたテキストのタグに一致する検索キーです。 この値は、メッセージ間で比較的一意である必要があります。 
    
_lpAddressBook_
  
> [in]アドレスのエントリの識別子の情報を取得するために使用するアドレス帳のオブジェクトへのポインター。 
    
_lppTNEF_
  
> [out]新しい TNEF オブジェクトへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

**OpenTnefStreamEx** [OpenTnefStream](opentnefstream.md)TNEF のアクセスのための元のエントリ ポイントの交換をお勧めします。 
  
TNEF オブジェクトが後で、 **OpenTnefStreamEx**関数によって作成された OLE メソッド サポート オブジェクト、ストリーム オブジェクト、およびメッセージのオブジェクトへの参照を追加するのには**IUnknown::AddRef**を呼び出します。 トランスポート プロバイダーは、OLE**が**オブジェクトのメソッド、TNEF を 1 回の呼び出しですべての 3 つのオブジェクトの参照を解放できます。 
  
**OpenTnefStreamEx** TNEF ストリーム メッセージを MAPI メッセージのエンコードに使用するプロバイダーの TNEF のオブジェクトを初期化します。 代わりに、この関数は、MAPI メッセージに TNEF ストリーム メッセージをデコードするのには[ITnef::ExtractProps](itnef-extractprops.md)以降の呼び出しに使用するプロバイダーのオブジェクトを設定できます。 TNEF オブジェクトを解放し、セッションを閉じる、トランスポート プロバイダーはオブジェクトの継承**が**メソッドを呼び出す必要があります。 
  
_WKeyVal_パラメーターの基本値は 0 にできませんする必要があり、 **OpenTnefStreamEx**を呼び出すたびに同じにしないで。 代わりに、実行時ライブラリの乱数生成器からのシステム時間に基づく乱数を使用します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI では、 **OpenTnefStreamEx**メソッドを使用して、プロパティを抽出することがありますので、TNEF ファイル ストリームをオープンします。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

