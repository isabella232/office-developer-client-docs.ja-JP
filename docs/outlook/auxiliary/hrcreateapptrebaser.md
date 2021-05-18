---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: IOlkApptRebaser オブジェクトを初期化して、予定表の予定を再Outlookします。
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317613"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

[IOlkApptRebaser](iolkapptrebaser.md)オブジェクトを初期化して、予定表の予定を再Outlookします。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tzmovelib.h  <br/> |
|実装元:  <br/> |tzmovelib.dll  <br/> |
|呼び出し元:  <br/> |MAPI クライアント アプリケーション  <br/> |
|ポインターの種類:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|DLL エントリ ポイント:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a>パラメーター

_ulFlags_
  
> [in]必要があります。 再調整の実行方法を制御するために使用されるフラグのビットマスク。 次のフラグを設定し、tzmovelib.h で定義できます。
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —ユーザーが会議開催者である予定アイテムが再ベースされます。 既定では、会議の更新Outlook、再ベースされている会議のすべての出席者に送信されます。 このフラグを会議の更新プログラムまたは **REBASE_FLAG_FORCE_NO_EX_UPDATESまたはREBASE_FLAG_FORCE_NO_UPDATES** して、 **会議の更新** の処理方法を変更できます。 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** — タイム ゾーンでマークされていない予定アイテムを更新します。 このフラグを指定すると  *、pTZMissing*  値は、タイム ゾーン データを持つすべてのアイテムに対してアイテムが作成されるタイム ゾーンとして使用されます。 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** —定期的な予定アイテムのみを更新します。 
    
   - **REBASE_FLAG_NO_UI** —メッセージ ストアを開く際に一般的に表示されるログオン ダイアログ ボックスを含む、ユーザー インターフェイス (UI) を表示しない。 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —過去に発生した予定アイテムを再ベースにしません。 
    
   - **REBASE_FLAG_FORCE_REBASE** —開催者に決定の再送信を確認しないが、ユーザーが出席者である予定アイテムを再ベース化します。 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** —ユーザーがオーガナイザーであり、受信者がユーザーに接続されていない場合にのみ更新プログラムを送信Exchange Server。 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** —更新プログラムを送信しない。 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —更新プログラムが適用される前に作成された単一インスタンスの予定アイテムのみをリベースします。 
    
   - **REBASE_FLAG_REPORTING_MODE** —実際にはリベースを行うのではなく、リベースされる予定アイテムを報告してください。 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** —会議の更新プログラムをリソースに送信します。 
    
_pSession_
  
> [in]必要があります。 MAPI セッション インターフェイスへのポインター。
    
_pCalendarMsgStore_
  
> [in]必要があります。 リベースする予定アイテムを含むメッセージ ストアへのポインター。
    
_pCalendarFolder_
  
> [in]必要があります。 再ベースする予定アイテムを含む予定表フォルダーへのポインター。
    
_pwszUpdatePrefix_
  
> [in]省略可能です。 会議出席依頼の先頭に付加されるプレフィックスを含む文字列へのポインター。 NULL の場合があります。
    
_pftInstallDateUTC_
  
> [in]省略可能です。 タイム ゾーンパッチのインストール日。 このフラグ **がREBASE_FLAG_ONLY_CREATED_PRE_PATCH場合** にのみ使用されます。 
    
_IExpansionDepth_
  
> [in]省略可能です。 配布リストを展開して、配布リストに接続されている受信者を除外する場合の拡張Exchange Server。 このフラグが設定されている **REBASE_FLAG_FORCE_NO_EX_UPDATES** のみ使用されます。 
    
_pTZTo_
  
> [in]必要があります。 再ベースするタイム ゾーンを記述する **TZDEFINITION** 構造体へのポインター。 **TZDEFINITION は** tzmovelib で定義されます。 
    
pTZMissing
  
> [in]必要があります。 タイム ゾーン情報がアイテムにスタンプされていない場合に想定されるタイム ゾーンを記述する **TZDEFINITION** 構造体へのポインター。 NULL にすることはできませんが、このフラグが設定されている **REBASE_FLAG_UPDATE_UNMARKED使用してください** 。 
    
_ppError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。 拡張エラー情報が必要ない場合は NULL を指定できます。 [MAPIFreeBuffer で無料](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx)です。 
    
_ppApptRebase_
  
> [out]返される **IOlkApptRebaser インターフェイスへのポインターを指すポインター** 。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

[GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx)を使用してこの関数のアドレスを検索する場合は **tzmovelib.dllプロシージャHrCreateApptRebaser@44** として指定します。 すべてのフラグが互いに組み合わせて有効な場合ではありません。 
  
さまざまなオプションの詳細については、KB [931667](https://support.microsoft.com/kb/931667/en-us)の「Outlook タイム ゾーン データ更新ツールのコマンド ライン オプションの用語集」を参照してください。Microsoft Office Outlook のタイム ゾーン データ更新ツールを使用してタイム ゾーンの変更に対処する方法。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

