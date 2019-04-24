---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346642"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi サブシステムの参照カウントを増分し、mapi DLL のグローバルデータを初期化します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapix  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>パラメーター

 _lpMapiInit_
  
> 順番[MAPIINIT_0](mapiinit_0.md)構造体へのポインター。 _lpMapiInit_パラメーターは NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> MAPI サブシステムは正常に初期化されました。
    
## <a name="remarks"></a>解説

**MAPIInitialize**関数は mapi サブシステムの mapi 参照カウントをインクリメントし、 [MAPIUninitialize](mapiuninitialize.md)関数は内部参照カウントをデクリメントします。 そのため、1つの関数への呼び出しの数は、もう一方への呼び出しの数と等しくなければなりません。 MAPI が以前に初期化されていない場合、 **MAPIInitialize**は S_OK を返します。 
  
クライアントまたはサービスプロバイダーは、他の MAPI 呼び出しを行う前に**MAPIInitialize**を呼び出す必要があります。 失敗すると、クライアントまたはサービスプロバイダーの呼び出しが MAPI_E_NOT_INITIALIZED の値を返します。 
  
マルチスレッドアプリケーションから**MAPIInitialize**を呼び出すときは、 _lpMapiInit_パラメーターを次のように宣言されている[MAPIINIT_0](mapiinit_0.md)構造に設定します。 
  
 **MAPIINIT_0**MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
そして、次のように呼び出します。 
  
 **MAPIInitialize**(&amp;MAPIINIT); 
  
この構造体を宣言すると、MAPI は通知ウィンドウを処理する別のスレッドを作成します。これは、初期化の参照カウントが0になるまで続行します。 Windows サービスでは、 _lpMapiInit_によって参照されている**MAPIINIT_0**構造体の**ulflags**メンバーを MAPI_NT_SERVICE に設定する必要があります。 
  
> [!NOTE]
> **MAPIInitialize**または**MAPIUninitialize**は、Win32 **DllMain**関数から、またはスレッドを作成または終了する他の関数内から呼び出すことはできません。 詳細については、「[スレッドセーフオブジェクトの使用](using-thread-safe-objects.md)」を参照してください。 
  
 **MAPIInitialize**では、拡張エラー情報は返されません。 他のほとんどの MAPI 呼び出しとは異なり、戻り値の意味は、エラーが発生した初期化の特定の手順に対応するように厳密に定義されます。 
  
1. パラメーターとフラグをチェックします。
    
    MAPI_E_INVALID_PARAMETER または MAPI_E_UNKNOWN_FLAGS。 発信者が無効なパラメーターまたはフラグを渡しました。
    
2. MAPI に必要なレジストリキーを初期化し、オペレーティングシステムの種類を確認します。 この手順は、クライアントプロセスが Windows でサービスとして実行されていて、 **MAPIINIT_0**構造の MAPI_NT サービスフラグを設定している場合にのみ発生します。 
    
    MAPI_E_TOO_COMPLEX。 呼び出し元のプロセスは Windows サービスであり、MAPI に必要なレジストリキーを初期化できませんでした。 
    
    アプリケーションイベントログで追加情報を入手できる場合があります。
    
3. MAPI と ole が互換性があるかどうかを確認し、ole を初期化します。
    
1. 現在のバージョンの OLE と MAPI の間に互換性があるかどうかを確認します。 
    
    MAPI_E_VERSION。 ワークステーションにインストールされている OLE のバージョンは、このバージョンの MAPI と互換性がありません。
    
2. OLE を初期化します。 
    
    この手順では、この関数では、ここに記載されていないエラーコードを返すことができます。 ここに記載さ_れていない_エラーは、OLE 関数**CoInitialize**からのものであることを前提としています。
    
4. プロセスごとのグローバル変数を初期化します。
    
    MAPI_E_SESSION_LIMIT。 MAPI は、現在のプロセスに固有のコンテキストを設定します。 プロセスの数が特定の数を超えた場合、または使用可能なメモリが不足している場合は、Win16 でエラーが発生することがあります。
    
5. すべてのプロセスの共有グローバル変数を初期化します。
    
    MAPI_E_NOT_ENOUGH_RESOURCES。 システムリソースが不足しているため、操作を完了できませんでした。
    
6. 通知エンジンを初期化し、MAPI_MULTITHREAD_NOTIFICATIONS フラグによって要求された場合は、ウィンドウとそのスレッドを作成します。 
    
    MAPI_E_INVALID_OBJECT。 システムリソースが不足すると、エラーが発生することがあります。 
    
7. プロファイルプロバイダーを読み込んで初期化します。 **MAPIInitialize**がプロファイルデータが格納されているレジストリキーにアクセスできることを確認します。 
    
    MAPI_E_NOT_INITIALIZED。 プロファイルプロバイダーでエラーが発生しました。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> ||mfcmapi は、 **MAPIInitialize**メソッドを使用して、バックグラウンドスレッドで MAPI を初期化し、一部のテーブル処理を実行します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

