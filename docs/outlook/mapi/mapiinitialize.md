---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a632b9ccb31220620ae010dd52b7a147a02c050
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592110"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI サブシステム参照カウントをインクリメントし、MAPI DLL のグローバル データを初期化します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>パラメーター

 _lpMapiInit_
  
> [in]構造体への [ポインター](mapiinit_0.md) MAPIINIT_0します。 _lpMapiInit パラメーター_ は NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> MAPI サブシステムが正常に初期化されました。
    
## <a name="remarks"></a>注釈

**MAPIInitialize** 関数は MAPI サブシステムの MAPI 参照カウントをインクリメントし [、MAPIUninitialize](mapiuninitialize.md)関数は内部参照カウントをデクリメントします。 したがって、1 つの関数に対する呼び出しの数は、もう一方の関数への呼び出しの数と等しくする必要があります。 **MAPIInitialize は** 、MAPI S_OK初期化されていない場合は、この値を返します。 
  
クライアントまたはサービス プロバイダーは、他の MAPI 呼 **び出しを行う前に MAPIInitialize** を呼び出す必要があります。 そうしない場合、クライアントまたはサービス プロバイダーの呼び出しは、MAPI_E_NOT_INITIALIZEDします。 
  
マルチスレッド アプリケーション **から MAPIInitialize** を呼び出す場合は  _、lpMapiInit_ パラメーター [を次のように](mapiinit_0.md) 宣言された MAPIINIT_0 構造体に設定します。 
  
 **MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
と呼び出し: 
  
 **MAPIInitialize** &amp; (MAPIINIT); 
  
この構造体を宣言すると、MAPI は通知ウィンドウを処理する別のスレッドを作成します。これは、初期化参照カウントが 0 になるまで続きます。 サービス _Windows、lpMapiInit_ が指す MAPIINIT_0構造体の **ulflags** メンバーを、MAPI_NT_SERVICE。 
  
> [!NOTE]
> Win32 **DllMain** 関数またはスレッドを作成または終了するその他の関数内から **MAPIInitialize** または **MAPIUninitialize** を呼び出す必要があります。 詳細については、「Using [Thread-Safe オブジェクト」を参照してください](using-thread-safe-objects.md)。 
  
 **MAPIInitialize では** 、拡張エラー情報は返されません。 他のほとんどの MAPI 呼び出しとは異なり、戻り値の意味は、失敗した初期化の特定の手順に対応するために厳密に定義されます。 
  
1. パラメーターとフラグをチェックします。
    
    MAPI_E_INVALID_PARAMETERまたはMAPI_E_UNKNOWN_FLAGS。 呼び出し元が無効なパラメーターまたはフラグを渡しました。
    
2. MAPI で必要なレジストリ キーを初期化し、オペレーティング システムの種類を確認します。 この手順は、クライアント プロセスが Windows の下でサービスとして実行され、MAPI_NT SERVICE フラグを MAPIINIT_0する **場合にのみMAPIINIT_0** されます。 
    
    MAPI_E_TOO_COMPLEX。 呼び出しプロセスはWindowsサービスであり、MAPI で必要なレジストリ キーを初期化できませんでした。 
    
    その他の情報は、アプリケーション イベント ログで確認できます。
    
3. MAPI と OLE の互換性を確認し、OLE を初期化します。
    
1. OLE と MAPI の現在のバージョン間の互換性を確認します。 
    
    MAPI_E_VERSION。 ワークステーションにインストールされている OLE のバージョンは、このバージョンの MAPI と互換性がありません。
    
2. OLE を初期化します。 
    
    この手順の間のみ、この関数はここに記載されていないエラー コードを返す場合があります。 ここに記載  _されていない_ エラーは、OLE 関数 **CoInitialize からのエラーと見なす必要があります**。
    
4. プロセスごとのグローバル変数を初期化します。
    
    MAPI_E_SESSION_LIMIT。 MAPI は、現在のプロセスに固有のコンテキストを設定します。 Win16 では、プロセス数が一定の数を超えた場合、または使用可能なメモリが使い果たされた場合はシステム上でエラーが発生する可能性があります。
    
5. すべてのプロセスの共有グローバル変数を初期化します。
    
    MAPI_E_NOT_ENOUGH_RESOURCES。 操作を完了するのに十分なシステム リソースが使用できません。
    
6. 通知エンジンを初期化し、ウィンドウとそのスレッドを作成します (このフラグで要求された場合MAPI_MULTITHREAD_NOTIFICATIONSします。 
    
    MAPI_E_INVALID_OBJECT。 システム リソースが使い果たされた場合、失敗する可能性があります。 
    
7. プロファイル プロバイダーを読み込み、初期化します。 **MAPIInitialize がプロファイル** データが格納されているレジストリ キーにアクセスできると確認します。 
    
    MAPI_E_NOT_INITIALIZED。 プロファイル プロバイダーでエラーが発生しました。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI では **、MAPIInitialize** メソッドを使用して、バックグラウンド スレッドで MAPI を初期化して、テーブル処理を実行します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

