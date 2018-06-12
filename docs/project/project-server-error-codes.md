---
title: Project Server エラー コード
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- error codes
- errors
- Project Server errors
- PSErrorID
- PSI errors
keywords:
- psi、エラー コード、エラー コードをプロジェクトのサーバー、PSErrorID、プロジェクトのサーバーのインターフェイス、エラー コード、プロジェクトのサーバーのエラー コード
localization_priority: Normal
ms.assetid: db78a09c-ebef-47cc-8623-40abe117aa08
description: このトピックには、Project Server 2013 のプロジェクト Server インターフェイス (PSI) のエラー コードのテーブルが含まれています。 機能領域とエラー ・ コードの範囲によっては、テーブルが配置されます。
ms.openlocfilehash: 9d63ed0dde638d123098ec4ffb8de083ddbb4fc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804723"
---
# <a name="project-server-error-codes"></a>Project Server エラー コード

このトピックには、Project Server 2013 のプロジェクト Server インターフェイス (PSI) のエラー コードのテーブルが含まれています。 機能領域とエラー ・ コードの範囲によっては、テーブルが配置されます。
   
Project Server 2013 のプロセスと、アドインの機能領域で一般に配置されたエラー コード番号があります。 [Microsoft.Office.Project.Server.Library.PSErrorID](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSErrorID.aspx)列挙型と重複して[WebSvcProject.PSErrorID](https://msdn.microsoft.com/library/WebSvcProject.PSErrorID.aspx)。名でアルファベット順のエラー コードをリスト表示します。 このトピックでは、PSI クラスまたは機能領域、およびエラーの識別子 (ID) 番号に配置されたテーブルのエラー コードを示します。 
  
> [!NOTE]
>  エラー コードの多くは汎用的なもので、複数の原因が考えられることもあります。エラーの詳細を調べるには、次の方法があります。 
> - ASMX ベースのアプリケーションでは、PSI メソッドの呼び出しでリストまたはエラーの階層を表示するのに**PSClientError**オブジェクトに**System.Web.Services.Protocols.SoapException**を使用します。 [ASMX のエラー コードの例](#pj15_ErrorCodes_ASMXExample)を参照してください。 
> - WCF ベースのアプリケーションでは、 **PSClientError**オブジェクトを取得し、追加のエラー情報を取得する**System.ServiceModel.FaultException**を使用できます。 [WCF のエラー コードの例](#pj15_ErrorCodes_WCFExample)を参照してください。 
> - Project Server コンピューター上のアプリケーション イベント ログを使用する。
> - ユニファイド ログ サービス (ULS) のトレース ログを使用します。 詳細については、 [Project 2010 の開発を開始する](http://msdn.microsoft.com/en-us/library/gg607685.aspx)*エラーをチェック*する」を参照してください。 
> - 詳細については、ULS ログを使用して、プロジェクトのサポートのブログの記事を参照してください[Project Server 2010: 予期、予期しないを取得する場合にどのような](http://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx)のブログを検索して「ログ ULS を読む」 
> - 検索または ULS データ内の特定の問題を監視するために、するには、 [ULS ビューアー](http://www.codeproject.com/Articles/458052/ULS-Log-Viewer)を使用します。 
> - キャッチしたり、データベースのエラーを監視するのにには、Microsoft SQL Server プロファイラーを使用します。 詳細については、 [SQL Server プロファイラー](http://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx)を参照してください。 
> - エラー コードの多くは、内部でのみ使用されています。 たとえば、 **ExchangeSync** 、 **PWA** web サービスは、サードパーティの開発ではサポートされていません、ためする**ルール**および**StatusReports**メソッドなど、これらの領域内のメソッドからエラー コードが表示される可能性ではできません。 ただし、この記事の表には、完全を期すのため、すべての Project Server エラー コードが含まれます。 
  
## <a name="table-1-error-code-functional-areas-and-related-number-ranges"></a>表 1. エラー コードの機能領域と関連する数値の範囲

|サーバーの機能領域をプロジェクトします。|エラー コードの数値の範囲|
|:-----|:-----|
|[表 3: 一般的なエラー コード](#pj15_ErrorCodes_General) <br/> |0 - 99 です。500-999 です。9131;10000-10099 です。20000-20099 です。26000-26099  <br/> |
|[表 4: アクティブなキャッシュ](#pj15_ErrorCodes_ActiveCache) <br/> |12000-12099  <br/> |
|[表 5: Active Directory の同期](#pj15_ErrorCodes_ActiveDirectory) <br/> |27000-27999  <br/> |
|[表 6: 管理 web サービス](#pj15_ErrorCodes_Admin) <br/> |16600 ～ 16699、19011、19012、19032、20003、25000 ～ 25099  <br/> |
|[(バックアップと復元)、表 7: アーカイブ](#pj15_ErrorCodes_Archive) <br/> |25000 ～ 25999、29000 ～ 29099  <br/> |
|[表 8: 割り当て](#pj15_ErrorCodes_Assignments) <br/> |120-199  <br/> |
|[表 9: カレンダー](#pj15_ErrorCodes_Calendar) <br/> |77、13000 ～ 13999  <br/> |
|[表 10: キューブ作成サービス (CBS)](#pj15_ErrorCodes_CBS) <br/> |17000-17999  <br/> |
|[表 11: チェックイン、チェック アウト](#pj15_ErrorCodes_CICO) <br/> |10100-10199  <br/> |
|[表 12: ユーザー設定フィールド](#pj15_ErrorCodes_CustomFields) <br/> |11500-11999  <br/> |
|[表 13: ルックアップ テーブル](#pj15_ErrorCodes_LookupTables) <br/> |11000-11499  <br/> |
|[表 14: その他](#pj15_ErrorCodes_Miscellaneous) <br/> |11000-11499  <br/> |
|[表 15: 通知](#pj15_ErrorCodes_Notifications) <br/> |16000-16599  <br/> |
|[表 16: オプティマイザー](#pj15_ErrorCodes_Optimizer)(プロジェクト ポートフォリオ分析)  <br/> |29000-29999  <br/> |
|[表 17: プランナー](#pj15_ErrorCodes_Planner)(プロジェクト ポートフォリオ分析)  <br/> |28000-28999  <br/> |
|[表 18: プロジェクト](#pj15_ErrorCodes_Projects) <br/> |100-499 です。1000-1199。9100-9199 です。23000 23999  <br/> |
|[表 19: レポート データ サービス](#pj15_ErrorCodes_RDS)(RDS)  <br/> |24000-24999  <br/> |
|[表 20: リソース](#pj15_ErrorCodes_Resources) <br/> |2000-2999  <br/> |
|[表 21: リソース計画](#pj15_ErrorCodes_ResourcePlans) <br/> |30000-30999  <br/> |
|[表 22: ルール](#pj15_ErrorCodes_Rules) <br/> |21000 から 21099  <br/> |
|[表 23: セキュリティ](#pj15_ErrorCodes_Security) <br/> |19000-19099  <br/> |
|[表 24: サーバーのイベント](#pj15_ErrorCodes_Events) <br/> |19033、22000 ～ 22999  <br/> |
|[表 25: 状態管理](#pj15_ErrorCodes_Statusing) <br/> |3100-3199  <br/> |
|[表 26: 進捗レポート](#pj15_ErrorCodes_StatusReports) <br/> |12100-12299  <br/> |
|[表 27: タスク](#pj15_ErrorCodes_Tasks) <br/> |7000-7099  <br/> |
|[表 28: タイムシート](#pj15_ErrorCodes_Timesheets) <br/> |3200-3299  <br/> |
|[表 29: ユーザーの委任](#pj15_ErrorCodes_UserDelegation) <br/> |43000-43500  <br/> |
|[表 30: ワークフロー](#pj15_ErrorCodes_Workflow) <br/> |35000 ～ 35999: ワークフロー  <br/> |
|[表 31: WSSInterop と ObjectLinkProvider (SharePoint の統合)](#pj15_ErrorCodes_WSS) <br/> |16400 ～ 16499: SharePoint 統合とプロジェクト ワークスペース  <br/> 18000 ～ 18099: オブジェクト リンク プロバイダーと SharePoint プロジェクトのインポート  <br/> |
   
## <a name="table-2-error-code-table-by-number-range"></a>表 2. 数値の範囲によるエラー コードの表

|エラー ・ コードの範囲|エラーコード表|
|:-----|:-----|
|0 - 99  <br/> |[表 3: 一般的なエラー コード](#pj15_ErrorCodes_General)では、77 点を除いて、[表 9: カレンダー](#pj15_ErrorCodes_Calendar) <br/> |
|100-119  <br/> |[表 18: プロジェクト](#pj15_ErrorCodes_Projects) <br/> |
|120-199  <br/> |[表 8: 割り当て](#pj15_ErrorCodes_Assignments) <br/> |
|500-999  <br/> |[表 3: 一般的なエラー コード](#pj15_ErrorCodes_General) <br/> |
|1000-1199  <br/> |[表 18: プロジェクト](#pj15_ErrorCodes_Projects) <br/> |
|2000-2999  <br/> |[表 20: リソース](#pj15_ErrorCodes_Resources) <br/> |
|3100-3199  <br/> |[表 25: 状態管理](#pj15_ErrorCodes_Statusing) <br/> |
|3200-3299  <br/> |[表 28: タイムシート](#pj15_ErrorCodes_Timesheets) <br/> |
|7000-7099  <br/> |[表 27: タスク](#pj15_ErrorCodes_Tasks) <br/> |
|9100-9199  <br/> |[表 18: プロジェクト](#pj15_ErrorCodes_Projects)9131 がある点を除いて、[表 3: 一般的なエラー コード](#pj15_ErrorCodes_General) <br/> |
|10000-10099  <br/> |[表 3: 一般的なエラー コード](#pj15_ErrorCodes_General) <br/> |
|10100-10199  <br/> |[表 11: チェックイン、チェック アウト](#pj15_ErrorCodes_CICO) <br/> |
|11000-11499  <br/> |[表 13: ルックアップ テーブル](#pj15_ErrorCodes_LookupTables) <br/> |
|11500-11999  <br/> |[表 12: ユーザー設定フィールド](#pj15_ErrorCodes_CustomFields) <br/> |
|12000-12099  <br/> |[表 4: アクティブなキャッシュ](#pj15_ErrorCodes_ActiveCache) <br/> |
|12100-12299  <br/> |[表 26: 進捗レポート](#pj15_ErrorCodes_StatusReports) <br/> |
|13000-13999  <br/> |[表 9: カレンダー](#pj15_ErrorCodes_Calendar) <br/> |
|16000-16399  <br/> |[表 15: 通知](#pj15_ErrorCodes_Notifications) <br/> |
|16400-16499  <br/> |[表 31: WssInterop とオブジェクト リンク プロバイダー (SharePoint の統合)](#pj15_ErrorCodes_WSS) <br/> |
|16600-16699  <br/> |[表 6: 管理 web サービス](#pj15_ErrorCodes_Admin) <br/> |
|17000-17999  <br/> |[表 10: キューブ作成サービス (CBS)](#pj15_ErrorCodes_CBS) <br/> |
|18000-18099  <br/> |[表 31: SharePoint の統合](#pj15_ErrorCodes_WSS) <br/> |
|19000-19099  <br/> |[表 23: セキュリティ](#pj15_ErrorCodes_Security): 19011、19012、19032 は、内のコードのセキュリティに関連する点を除いて、[表 6: 管理 web サービス](#pj15_ErrorCodes_Admin) <br/> |
|20000-20099  <br/> |[表 3: 一般的なエラー コード](#pj15_ErrorCodes_General)20003 がある点を除いて、[表 6: 管理 web サービス](#pj15_ErrorCodes_Admin) <br/> |
|21000 から 21099  <br/> |[表 22: ルール](#pj15_ErrorCodes_Rules) <br/> |
|22000-22999  <br/> |[表 24: サーバーのイベント](#pj15_ErrorCodes_Events) <br/> |
|23000-23999  <br/> |[表 18: プロジェクト](#pj15_ErrorCodes_Projects) <br/> |
|24000-24999  <br/> |[表 19: レポート データ サービス](#pj15_ErrorCodes_RDS)(RDS)  <br/> |
|25000-25999  <br/> |[表 7: アーカイブ (バックアップと復元)](#pj15_ErrorCodes_Archive)を除く 25004、25006 は[表 6: 管理 web サービス](#pj15_ErrorCodes_Admin) <br/> |
|26000-26099  <br/> |[表 3: 一般的なエラー コード](#pj15_ErrorCodes_General) <br/> |
|27000-27999  <br/> |[表 5: Active Directory の同期](#pj15_ErrorCodes_ActiveDirectory) <br/> |
|28000-28999  <br/> |[表 17: プランナー](#pj15_ErrorCodes_Planner)(プロジェクト ポートフォリオ分析)  <br/> |
|29000-29999  <br/> |[表 16: オプティマイザー](#pj15_ErrorCodes_Optimizer)(プロジェクト ポートフォリオ分析)、29021 がある点を除いて[表 7: アーカイブ](#pj15_ErrorCodes_Archive) <br/> |
|30000-30999  <br/> |[表 21: リソース計画](#pj15_ErrorCodes_ResourcePlans) <br/> |
|31000-31999  <br/> 32000-32100  <br/> |[表 14: その他](#pj15_ErrorCodes_Miscellaneous)(監査は使用されません)  <br/> プロジェクト詳細ページ  <br/> |
|35000-35999  <br/> 40000-40499  <br/> |[表 30: ワークフロー](#pj15_ErrorCodes_Workflow) <br/> |
|40500-40999  <br/> 42000-42999  <br/> |[表 14: その他](#pj15_ErrorCodes_Miscellaneous)(**ExchangeSync**内部で使用)。  <br/> Project Web App のタイムライン  <br/> |
|43000-43500  <br/> |[表 29: ユーザーの委任](#pj15_ErrorCodes_UserDelegation) <br/> |
|50000-51999  <br/> |[表 14: その他](#pj15_ErrorCodes_Miscellaneous)(データベース エラーが発生)  <br/> |

<a name="pj15_ErrorCodes_General"></a>

## <a name="table-3-general-error-codes"></a>表 3. 一般的なエラー コード

|一般的なエラー コード|説明|
|:-----|:-----|
|NoError = 0、Success = 0  <br/> |エラーなし、または成功。  <br/> |
|GeneralRequestInvalidParameter = 6  <br/> |要求ノードまたはパラメーターの 1 つが無効であるか、要求のコンテキスト内部で無効です。  <br/> |
|GeneralInvalidValue = 11  <br/> |要求値が無効。0 として指定されている GUID など。  <br/> |
|GeneralStartDateGTorEQFinishDate = 26  <br/> |指定されている日付範囲が無効です。  <br/> |
|GeneralQueueOperationInProcess = 29  <br/> |まだキューで処理されている操作に関する一般的なエラー。  <br/> |
|GeneralUnhandledException = 42  <br/> |処理されない例外が発生しました。  <br/> |
|GeneralDuplicateGUIDSpecified = 66  <br/> |要求に重複する GUID があります。  <br/> |
|GeneralDateNotValid = 69  <br/> |日付は 1/1/1984 から 12/12/2049 の範囲に存在する必要があります。  <br/> |
|GeneralCostInvalid = 70  <br/> |コスト パラメーターが無効です。  <br/> |
|GeneralWorkInvalid = 71  <br/> |作業パラメーターが無効です。  <br/> |
|GeneralDurationInvalid = 72  <br/> |期間パラメーターが無効です。  <br/> |
|GeneralUnitsInvalid = 73  <br/> |指定されている単位が無効です。  <br/> |
|GeneralOnlyInsertsAllowed = 74  <br/> |挿入のみが許可されています。  <br/> |
|GeneralOnlyUpdatesAllowed = 75  <br/> |更新のみが許可されています。  <br/> |
|GeneralSessionInvalid = 76  <br/> |セッション パラメーターが無効です。  <br/> |
|GeneralDependencyUidInvalid = 78  <br/> |依存関係 GUID が無効です。  <br/> |
|GeneralNumberInvalid = 79  <br/> |数値が無効です。  <br/> |
|GeneralInvalidDataStore = 80  <br/> |指定されたデータベースが存在しません。 [DataStoreEnum](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.DataStoreEnum.aspx)では、データベースを使用します。  <br/> |
|GeneralDurationOrWorkFormatInvalid = 513  <br/> |作業の期間または形式が無効です。  <br/> |
|GeneralRateFormatInvalid = 518  <br/> |単価の形式が無効です。  <br/> |
|GeneralQueueException = 9131  <br/> |例外: キュー サービスで一般エラーが発生しました。  <br/> |
|GeneralItemDoesNotExist = 10000  <br/> |指定されたアイテムが存在しません。  <br/> |
|GeneralLCIDInvalid = 10001  <br/> |ロケール識別子 (言語 ID) が無効です。  <br/> |
|GeneralRowDoesNotExist = 10002  <br/> |**データ テーブル**内の指定された行が存在しません。  <br/> |
|GeneralInvalidColumnValue = 20000  <br/> |**データ テーブル**の列の値が有効ではありません。  <br/> |
|GeneralInvalidDataRowState = 20001  <br/> |**DataRow**の状態が有効ではありません。  <br/> |
|GeneralDuplicatedNames = 20004  <br/> |重複する名前が存在します。名前は一意である必要があります。  <br/> |
|GeneralReadOnlyColumn = 20005  <br/> |列は読み取り専用です。  <br/> |
|GeneralReadOnlyRow = 20006  <br/> |行は読み取り専用です。  <br/> |
|GeneralNotNullColumn = 20007  <br/> |列を null にすることはできません。  <br/> |
|GeneralObjectAlreadyExists = 20008  <br/> |オブジェクトが既に存在します。  <br/> |
|GeneralInvalidObject = 20009  <br/> |オブジェクトが無効です。  <br/> |
|GeneralSecurityAccessDenied = 20010  <br/> |セキュリティ権限によりアクセスが拒否されました。  <br/> |
|GeneralInvalidOperation = 20011  <br/> |操作が無効です。  <br/> |
|GeneralInvalidCharacters = 20012  <br/> |いくつかの文字が有効ではありません。 だけでなく、タブ文字では、次の文字は、プロジェクト名に: ' \ と":;< > | , . ' ? * #` <br/> |
|GeneralNameTooLong = 20013  <br/> |名前が長すぎます。  <br/> |
|GeneralNameCannotBeBlank = 20014  <br/> |名前を空白にすることはできません。null または空白文字列を使用しないでください。  <br/> |
|GeneralInvalidOperationOnReadOnlyValue = 20016  <br/> |読み取り専用の値に対して試行された操作は無効です。  <br/> |
|GeneralInvalidDateOverlap = 20018  <br/> |要求には重なる日付が含まれています。  <br/> |
|GeneralParameterCannotBeNull = 20020  <br/> |パラメーターを null にすることはできません。  <br/> |
|GeneralDescTooLong = 20021  <br/> |説明が長すぎます。  <br/> |
|GeneralCategoryPermissionDenied = 20022  <br/> |カテゴリ権限が拒否されました。  <br/> |
|GeneralNotLicensed = 20024  <br/> |ユーザーには Project Server のライセンスがありません。  <br/> |
|GeneralGlobalPermissionDenied = 20023  <br/> |グローバル アクセス権が拒否されました。  <br/> |
|GeneralActionCanceledByEventHandler = 22000  <br/> |イベント ハンドラーがアクションをキャンセルしました。  <br/> |
|GeneralActionCanceledBecauseServerEventServiceNotFound = 22001  <br/> |Project Server イベント サービス が見つかりません。  <br/> |
|GeneralActionCanceledBecauseServerEventServiceProblem = 22002  <br/> |Project Server イベント サービス に問題があります。  <br/> |
|GeneralQueueJobFailed = 26000  <br/> |キュー ジョブが失敗しました。  <br/> |
|GeneralQueueInvalidJobUID = 26001  <br/> |キューのジョブ GUID が無効です。  <br/> |
|GeneralQueueInvalidTrackingUID = 26002  <br/> |キューの追跡用の GUID が無効です。  <br/> |
|GeneralQueueInvalidJobInfoUID = 26003  <br/> |キューのジョブ情報 GUID が無効です。  <br/> |
|GeneralQueueInvalidCorrelationUID = 26004  <br/> |キュー依存関係 GUID が無効です。  <br/> |
|GeneralQueueCorrelationBlocked = 26005  <br/> |キュー相互関係がブロックされました。  <br/> |
|GeneralQueueInvalidMessageType = 26006  <br/> |キューのメッセージの種類が無効です。  <br/> |
|GeneralQueueInvalidJobState = 26007  <br/> |キューのジョブの状態が無効です。  <br/> |
|GeneralQueueInvalidGroupState = 26008  <br/> |キューのグループの状態が無効です。  <br/> |
|GeneralQueueInvalidGroupPriority = 26009  <br/> |キューのグループの優先度が無効です。  <br/> |
|GeneralQueueInvalidCorrelationPriority = 26010  <br/> |キューの相互関係の優先度が無効です。  <br/> |
|GeneralQueueInvalidQueueID = 26011  <br/> |キューの識別番号が無効です。  <br/> |
|GeneralQueueInvalidAdminAction = 26012  <br/> |キューの**管理**操作が正しくありません。  <br/> |
|GeneralQueueInvalidStatType = 26013  <br/> |キューの状態の種類が無効です。  <br/> |
|GeneralQueueInvalidBlockPolicy = 26014  <br/> |キューのブロック ポリシーが無効です。  <br/> |
|GeneralQueueCannotRetryJob = 26015  <br/> |キューがジョブを再試行できません。  <br/> |
|GeneralQueueInvalidSetting = 26016  <br/> |キューの設定が無効です。  <br/> |
|GeneralQueueInvalidRendezvousUID = 26017  <br/> |キューのランデブー GUID が無効です。  <br/> |
|GeneralDalErrorGettingConnectionStrings = 26018  <br/> |データ アクセス層 (DAL) の接続文字列取得エラー。  <br/> |
|GeneralDalErrorConnectingToDatabase = 26019  <br/> |データベースに接続する DAL のエラー。  <br/> |
|GeneralDalInvalidArgumentCountCreatingFilter = 26020  <br/> |フィルターを作成するための引数の数が無効です。  <br/> |
|GeneralDataTableCannotBeNull = 26024  <br/> |**DataTable**を**null**にすることはできません。  <br/> |
|GeneralDatasetConstraints = 26025  <br/> |**データセット**の制約でエラーが発生しました。  <br/> |
|GeneralInvalidDataSetStructure = 26027  <br/> |**データセット**の構造が有効ではありません。  <br/> |
|GeneralDalNoRowsUpdated = 26028  <br/> |データ アクセス レイヤー (DAL) で行が更新されていません。  <br/> |
|GeneralDataTableCannotBeEmpty = 26029  <br/> |**データ テーブル**を空にすることはできません。  <br/> |
|GeneralWSSContentDBNotWritable = 26030  <br/> |SharePoint コンテンツ データベースに書き込めません。 コンテンツ データベースが読み取り専用か、サイト コレクションのレベルでロックがかかっています。  <br/> |
|GeneralSPValidateFormDigestError = 26031  <br/> |タイムアウトのため通常、Project Web App のコールバックのフォーム ダイジェストの検証でエラーが発生しました。  <br/> |
|GeneralDelegationActiveForCurrentUser = 26032  <br/> |現在のユーザーは、作業中の委任を持っています。 Project Professional の**WinProj**サービスの web メソッドでは、このエラーが発生します。  <br/> |

<a name="pj15_ErrorCodes_ActiveCache"></a>

## <a name="table-4-active-cache"></a>表 4. アクティブ キャッシュ

|アクティブ キャッシュのエラー コード|説明|
|:-----|:-----|
|ActiveCacheInvalidDataFormat = 12000  <br/> |データの形式が無効です。  <br/> |
|ActiveCacheUnsupportedDataFormatVersion = 12001  <br/> |データ形式のバージョンがサポートされていません。  <br/> |
|ActiveCacheInvalidQueuedMessageType = 12003  <br/> |キューに登録されたメッセージの種類が無効です。  <br/> |
|ActiveCacheNullQueuedMessage = 12004  <br/> |キューに登録されたメッセージが null です。  <br/> |
|ActiveCacheQueuedMessageExecutionError = 12005  <br/> |キューに登録されたメッセージに実行エラーが発生しました。  <br/> |
|ActiveCacheInvalidDataSize = 12006  <br/> |データのサイズが無効です。  <br/> |
|ActiveCacheQueueJobAlreadyStarted = 12007  <br/> |キューのジョブは既に開始しています。  <br/> |
|ActiveCacheInvalidQueuedMessageFormat = 12008  <br/> |キューのメッセージ形式が無効です。  <br/> |
|ActiveCacheUnsupportedQueuedMessageVersion = 12009  <br/> |キューのメッセージ バージョンが無効です。  <br/> |
|ActiveCacheUnsupportedQueueDataType = 12011  <br/> |キューのデータ型がサポートされていません。  <br/> |
|ActiveCacheInvalidVersionStampForSave = 12012  <br/> |保存操作のバージョン スタンプが無効です。  <br/> |
|ActiveCacheProjectTypeMismatch = 12013  <br/> |プロジェクトの種類が想定されている種類と一致しません。  <br/> |
|ActiveCacheDataValidationFailed = 12014  <br/> |データ検証に失敗しました。  <br/> |
|ActiveCacheUnsupportedProjectProfessionalVersion = 12015  <br/> |Project Professional のバージョンがサポートされていません。  <br/> |
|ActiveCacheGeneralSQLException = 12016  <br/> |一般 SQL エラーが発生しました。  <br/> |

<a name="pj15_ErrorCodes_ActiveDirectory"></a>

## <a name="table-5-active-directory-synchronization"></a>表 5. 作業中のディレクトリ同期

|アクティブなディレクトリ同期のエラー コード|説明|
|:-----|:-----|
|AdSyncUpdateTimerJobFailed = 27002  <br/> |Active Directory ディレクトリ サービスとの同期で、更新タイマー ジョブが失敗しました。  <br/> |
|AdSyncDeleteTimerJobFailed = 27003  <br/> |Active Directory との同期で、削除タイマー ジョブが失敗しました。  <br/> |
|AdSyncAdConnectFail = 27006  <br/> |Active Directory に接続できません。  <br/> |
|AdMaximumGroupsCountExceeded = 27007  <br/> |グループの最大数を超過しました。  <br/> |
|SRAInvalidVersion = 27300  <br/> |SRA のバージョンが無効です。  <br/> |
|SRADelayedUpgradeFailed = 27301  <br/> |SRA 非同期更新アクションが失敗しました。  <br/> |
|(27000-27999)  <br/> |Active Directory のその他の同期エラーは Project Server 内で列挙されません。  <br/> |

<a name="pj15_ErrorCodes_Admin"></a>

## <a name="table-6-admin-web-service"></a>表 6. 管理 web サービス

|管理 web サービスのエラー コード|説明|
|:-----|:-----|
|AdminViewNameAlreadyExists = 16600  <br/> |ビュー名が既に存在します。名前は一意である必要があります。  <br/> |
|AdminViewInvalidDividerPosition = 16601  <br/> |区切りの位置が無効です。  <br/> |
|AdminViewDataWasTampered = 16602  <br/> |データが変更されています。  <br/> |
|AdminViewMaxDisplayedFieldsNumberExceeded = 16603  <br/> |表示で、フィールドの最大数を超過しました。  <br/> |
|AdminViewCannotDeleteDefaultView = 16604  <br/> |既定のビューを削除できません。  <br/> |
|AdminViewCannotCopyDefaultView = 16605  <br/> |既定のビューをコピーできません。  <br/> |
|AdminLocalCustomFieldInvalid = 19011  <br/> |ローカル ユーザー設定フィールドが無効です。  <br/> |
|AdminEnterpriseCustomFieldInvalid = 19012  <br/> |エンタープライズ ユーザー設定フィールドが無効です。  <br/> |
|AdminNTAccountNotFound = 19032  <br/> |Windows (NTLM) アカウントが見つかりません。  <br/> |
|AdminUnableToMerge = 20003  <br/> |データをマージできません。  <br/> |
|AdminDeleteArchivedProjectsFailed = 25004  <br/> |アーカイブされたプロジェクトの削除操作が失敗しました。  <br/> |
|AdminUpdateArchiveScheduleFailed = 25006  <br/> |アーカイブ スケジュールの更新に失敗しました。  <br/> |
|AdminArchiveScheduleFailed = 28018  <br/> |アーカイブ スケジュールが失敗しました。  <br/> |
|AdminReadArchivedProjectsListFailed = 28019  <br/> |アーカイブされたプロジェクトのリストの読み込みに失敗しました。  <br/> |
|AdminReadArchiveScheduleFailed = 28020  <br/> |アーカイブ スケジュールの読み込みに失敗しました。  <br/> |
|AdminUserAccountNameNull = 28021  <br/> |ユーザー アカウント名が null です。  <br/> |
|AdminIsWindowsUserNull = 28022  <br/> |Windows (NTLM) ユーザー アカウントが null と表示されています。  <br/> |
|AdminInvalidTimePeriodState = 28023  <br/> |期間の状態が無効です。  <br/> |
|AdminGlobalUpdateFailed = 28024  <br/> |**SetServerCurrency**への呼び出し中に、エンタープライズ グローバルな更新ができませんでした。  <br/> |
|AdminGlobalCheckedOut = 28025  <br/> |エンタープライズ グローバル テンプレートは**SetServerCurrency**への呼び出し中に既にチェック アウトされています。  <br/> |
|AdminInvalidDatabaseTimeout = 28026  <br/> |データベースが無効なためタイムアウトしました。  <br/> |
|AdminInvalidDatabaseTimeoutType = 28027  <br/> |データベースの種類が無効なためタイムアウトしました。  <br/> |
|AdminInvalidEntityType = 28028  <br/> |エンティティの種類が正しくありません。 [EntityCollection](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.aspx)を参照してください。  <br/> |
|AdminInvalidCompatibilityModeChange = 28029  <br/> |互換性モードへの変更が無効です。  <br/> |
|AdminInvalidCompatibilityMode = 28030  <br/> |互換性モードが無効です。  <br/> |
|AdminInvalidProjectProfessionalVersions = 28031  <br/> |Project Professional の一連のバージョンが無効です。  <br/> |
|AdminInvalidProjectProfessionalVersion = 28032  <br/> |Project Professional のバージョンが無効です。  <br/> |
|AdminTooManyProjectProfessionalVersions = 28033  <br/> |指定した Project Professional のバージョンが多すぎます。  <br/> |
|AdminDuplicateProjectProfessionalMajorVersions = 28034  <br/> |Project Professional のメジャー バージョンが重複しています。 Project Professional 2007 をはじめとして、各メジャー リリースで指定できるバージョンは 1 つのみです。  <br/> |
|AdminInvalidServerFlags = 28035  <br/> |Project Server の設定の 1 つまたは複数のフラグが無効です。  <br/> |
|AdminNullProjectProfessionalVersions = 28036  <br/> |1 つまたは複数の Project Professional のバージョンが null です。  <br/> |

<a name="pj15_ErrorCodes_Archive"></a>

## <a name="table-7-archive-web-service"></a>表 7. アーカイブ web サービス

|アーカイブ web サービス (バックアップと復元) のエラー コード|説明|
|:-----|:-----|
|ArchiveProjectFailure = 25000  <br/> |プロジェクトのアーカイブ操作が失敗しました。  <br/> |
|ArchiveProjectsFailed = 25001  <br/> |アーカイブ データベースのプロジェクトを保存できません。  <br/> |
|ArchiveProjectFailed = 25002  <br/> |プロジェクトのアーカイブを保存できません。  <br/> |
|RestoreProjectFailed = 25003  <br/> |プロジェクトを復元できません。  <br/> |
|ArchiveResourcesFailed = 25007  <br/> |リソースのアーカイブを保存できません。  <br/> |
|ArchiveCustomFieldsFailed = 25008  <br/> |ユーザー設定フィールドのアーカイブを保存できません。  <br/> |
|RestoreCustomFieldsFailed = 25009  <br/> |ユーザー設定フィールドを復元できません。  <br/> |
|ArchiveSystemSettingsFailed = 25010  <br/> |システム設定のアーカイブを保存できません。  <br/> |
|RestoreSystemSettingsFailed = 25011  <br/> |システム設定を復元できません。  <br/> |
|ArchiveCategoriesFailed = 25012  <br/> |セキュリティ カテゴリのアーカイブを保存できません。  <br/> |
|RestoreCategoriesFailed = 25013  <br/> |セキュリティ カテゴリを復元できません。  <br/> |
|ArchiveViewsFailed = 25014  <br/> |ビュー アーカイブを保存できません。  <br/> |
|RestoreViewsFailed = 25015  <br/> |ビューを復元できません。  <br/> |
|ArchiveGlobalProjectFailed = 25016  <br/> |エンタープライズ グローバルのアーカイブを保存できません。  <br/> |
|RestoreGlobalProjectFailed = 25017  <br/> |エンタープライズ グローバル テンプレートを復元できません。  <br/> |
|ArchiveInvalidRetentionPolicyValue = 25018  <br/> |アーカイブ保持ポリシーの値が無効です。  <br/> |
|ArchiveCustomFieldsFailure = 25019  <br/> |ユーザー設定フィールドのアーカイブを読み込むことができません。  <br/> |
|ArchiveGlobalProjectFailure = 25020  <br/> |エンタープライズ グローバルのアーカイブを読み込むことができません。  <br/> |
|ArchiveResourcesFailure = 25021  <br/> |リソースのアーカイブを読み込むことができません。  <br/> |
|ArchiveSystemSettingsFailure = 25022  <br/> |システム設定のアーカイブを読み込むことができません。  <br/> |
|ArchiveViewsFailure = 25023  <br/> |ビューのアーカイブを読み込むことができません。  <br/> |
|ArchiveCategoriesFailure = 25024  <br/> |セキュリティ カテゴリのアーカイブを読み込むことができません。  <br/> |
|ResourcePlanPublishFailure = 25025  <br/> |リソース計画を発行できません。  <br/> |
|RestoreCategoriesFailure = 25026  <br/> |アーカイブからセキュリティ カテゴリを復元できません。  <br/> |
|RestoreCustomFieldsFailure = 25027  <br/> |アーカイブからユーザー設定フィールドを復元できません。  <br/> |
|RestoreGlobalProjectFailure = 25028  <br/> |アーカイブからエンタープライズ グローバル テンプレートを復元できません。  <br/> |
|RestoreProjectFailure = 25029  <br/> |アーカイブからプロジェクトを復元できません。  <br/> |
|RestoreResourcesFailure = 25030  <br/> |アーカイブからリソースを復元できません。  <br/> |
|RestoreSystemSettingsFailure = 25031  <br/> |アーカイブからシステム設定を復元できません。  <br/> |
|RestoreViewsFailure = 25032  <br/> |アーカイブからビューを復元できません。  <br/> |
|ArchiveReadProjectArchiveRetentionSettingFailed = 25033  <br/> |プロジェクトのアーカイブ保持の設定の読み込みに失敗しました。  <br/> |
|RestoreResourcesFailed = 29021  <br/> |リソースを復元できません。  <br/> |

<a name="pj15_ErrorCodes_Assignments"></a>

## <a name="table-8-assignment"></a>表 8. 割り当て

|割り当てのエラー コード|説明|
|:-----|:-----|
|AssignmentNotFound = 120  <br/> |割り当てが見つかりません。  <br/> |
|AssignmentWrongTrackingMethod = 122  <br/> |割り当ての進捗管理方法が正しくありません。  <br/> |
|AssignmentWorkTypeInvalid = 127  <br/> |割り当て作業時間の種類が無効です。  <br/> |
|AssignmentRateTableInvalid = 130  <br/> |割り当てのコスト単価表が無効です。  <br/> |
|AssignmentAlreadyExists = 131  <br/> |割り当てが既に存在します。  <br/> |
|AssignmentDuplicateSpecified = 132  <br/> |重複する割り当てが存在します。  <br/> |
|AssignmentUidInvalid = 133  <br/> |割り当て GUID が無効です。  <br/> |
|AssignmentDelayInvalid = 134  <br/> |割り当ての延期期間が無効です。  <br/> |
|AssignmentCannotEditSummaryTask = 135  <br/> |割り当てに対してサマリー タスクを編集できません。  <br/> |
|AssignmentInvalid = 136  <br/> |割り当てが無効です。  <br/> |
|AssignmentFieldsInvalidForBudget = 137  <br/> |予算に対して割り当てフィールドが無効です。  <br/> |
|AssignmentAlreadyAssignedToResource = 138  <br/> |リソースには既に割り当てが存在していました。  <br/> |
|AssignmentInvalidOwner = 139  <br/> |割り当て所有者が無効です。  <br/> |

<a name="pj15_ErrorCodes_Calendar"></a>

## <a name="table-9-calendar"></a>表 9. カレンダー

|カレンダーのエラー コード|説明|
|:-----|:-----|
|CalendarUidInvalid = 77  <br/> |カレンダー GUID が無効です。  <br/> |
|CalendarOnlyOneShiftIsNull = 13000  <br/> |1 つのシフトのみが null です。  <br/> |
|CalendarRecurrenceDaysShouldBeNull = 13001  <br/> |頻度日は null である必要があります。  <br/> |
|CalendarRecurrenceMonthDayShouldBeNull = 13002  <br/> |頻度月および頻度日は null である必要があります。  <br/> |
|CalendarRecurrenceMonthShouldBeNull = 13003  <br/> |頻度月は null である必要があります。  <br/> |
|CalendarRecurrenceMonthShouldNotBeNull = 13004  <br/> |頻度月を null にすることはできません。  <br/> |
|CalendarRecurrencePositionShouldBeNull = 13005  <br/> |頻度位置は null である必要があります。  <br/> |
|CalendarRecurrencePositionShouldNotBeNull = 13006  <br/> |頻度位置を null にすることはできません。  <br/> |
|CalendarRecurrenceDaysShouldNotBeNull = 13007  <br/> |頻度日を null にすることはできません。  <br/> |
|CalendarInvalidRecurrenceFrequency = 13008  <br/> |頻度が無効です。  <br/> |
|CalendarInvalidRecurrenceType = 13009  <br/> |頻度の種類が無効です。  <br/> |
|CalendarInvalidRecurrenceDays = 13010  <br/> |頻度日が無効です。  <br/> |
|CalendarInvalidCombinationOfMonthDayAndPosition = 13011  <br/> |月、日、および位置の組み合わせが無効です。  <br/> |
|CalendarInvalidRecurrencePosition = 13012  <br/> |頻度位置が無効です。  <br/> |
|CalendarCannotModifyExceptionsForCalendarBeingDeleted = 13013  <br/> |カレンダーが削除される際には、カレンダーの例外を変更できません。  <br/> |
|CalendarExceptionConflict = 13014  <br/> |カレンダーの例外に競合が存在します。  <br/> |
|CalendarBadDateValue = 13015  <br/> |日付が無効です。  <br/> |
|CalendarNotFound = 13021  <br/> |カレンダーが見つかりません。  <br/> |
|CalendarAlreadyExists = 13022  <br/> |カレンダーが既に存在します。  <br/> |
|CalendarNameShouldNotBeNull = 13023  <br/> |カレンダー名が null です。  <br/> |
|CalendarInternalError = 13025  <br/> |カレンダー操作で内部エラーが発生しました。  <br/> |
|CalendarNameTooLong = 13027  <br/> |カレンダー名が長すぎます。  <br/> |
|CalendarInvalidCalendarName = 13028  <br/> |カレンダー名が無効です。  <br/> |
|CalendarStandardCalendarNotFound = 13031  <br/> |標準カレンダーが見つかりません。  <br/> |
|CalendarInvalidShifts = 13032  <br/> |シフトが無効です。  <br/> |
|CalendarCannotDeleteCalendarUsedByProject = 13033  <br/> |プロジェクトで使用されているカレンダーを削除することはできません。  <br/> |
|CalCalendarUniqueIdToDuplicateShouldBeNull = 13035  <br/> |カレンダーを複製するには GUID は null である必要があります。  <br/> |
|CalendarInvalidBaseCalendarUniqueId = 13037  <br/> |基本カレンダー GUID が無効です。  <br/> |
|CalendarInvalidUniqueIdToDuplicate = 13038  <br/> |GUID が無効なため、カレンダーを複製できません。  <br/> |
|CalendarUnusedCalendarException = 13039  <br/> |カレンダーの例外には、対応する予定はありません。 **ResourceDataSet.CalendarExceptions**テーブルがない**BaseCalendarUniqueId**を [**リソース**] テーブルには、そのリソースのエントリがある場合は、 **UpdateResources**メソッドを使用するときに発生します。  <br/> |
|CalendarCannotDeleteStandardCalendar = 13040  <br/> |標準カレンダーを削除できません。  <br/> |
|CalendarCannotRenameStandardCalendar = 13041  <br/> |標準カレンダーの名前を変更できません。  <br/> |
|CalendarCannotDeleteCalendarUsedByEnterpriseResource = 13042  <br/> |カレンダーはエンタープライズ リソースにより使用されているため、削除できません。  <br/> |
|CalendarFilterInvalid = 13043  <br/> |カレンダーに対してフィルターが無効です。  <br/> |

<a name="pj15_ErrorCodes_CBS"></a>

## <a name="table-10-cubeadmin-and-cube-build-service"></a>表 10. CubeAdmin とキューブのサービスを構築します。

|CubeAdmin およびキューブ作成サービス (CBS) のエラー コード|説明|
|:-----|:-----|
|CBSGeneralFailure = 17001  <br/> |キューブ作成サービス (CBS) の失敗。これはさまざまな原因によって生じる一般的なエラー コードです。  <br/> |
|CBSDsoNotInstalled = 17002  <br/> |CBS には、Analysis Services 用にインストールされている Decision Support オブジェクト (DSO) コンポーネントが必要です。  <br/> |
|CBSASConnectionFailure = 17003  <br/> |CBS は Analysis Services サーバーへの接続に失敗しました。  <br/> |
|CBSOlapProcessingFailure = 17004  <br/> |OLAP キューブの処理に失敗しました。  <br/> |
|CBSMetadataProcessingFailure = 17005  <br/> |キューブのメタデータの処理に失敗しました。  <br/> |
|CBSASServerLockTimeOut = 17006  <br/> |Analysis Services サーバーのロックがタイムアウトしました。  <br/> |
|CBSOlapDatabaseSetupFailure = 17007  <br/> |OLAP キューブ データベースの設定に失敗しました。  <br/> |
|CBSASEntityLimitation = 17008  <br/> |Analysis Services が使用できるエンティティの数を超過しました。  <br/> |
|CBSRequestInvalidArguments = 17009  <br/> |CBS 要求の 1 つまたは複数の引数が無効です。  <br/> |
|CBSQueueingRequestFailed = 17010  <br/> |CBS はジョブをキューに送信するのに失敗しました。  <br/> |
|CBSUpdateCubeCalculatedMeasureDefintionError = 17011  <br/> |キューブ計算済みメンバーでエラーが発生しました。  <br/> |
|CBSAttemptToOverwrite = 17013  <br/> |キューブのデータを上書きできません。  <br/> |
|CBSCustomFieldCannotBeAddedAsDimension = 17014  <br/> |ユーザー設定フィールドをキューブ ディメンションにすることはできません。  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimension = 17015  <br/> |ユーザー設定フィールドをキューブのディメンションとして追加することに失敗しました。  <br/> |
|CBSCustomFieldCannotBeAddedAsMeasure = 17016  <br/> |ユーザー設定フィールドをキューブ メジャーにすることはできません。  <br/> |
|CBSCustomFieldFailedToBeAddedAsMeasure = 17017  <br/> |ユーザー設定フィールドをキューブのメジャーとして追加することに失敗しました。  <br/> |
|CBSDsoTranslatorNotFound = 17018  <br/> |Decision Support オブジェクト トランスレーターが見つかりません。  <br/> |
|CBSUpdateOlapDBOperationFailure = 17019  <br/> |OLAP データベースの更新に失敗しました。  <br/> |
|CBSOlapDBInvalidArguments = 17020  <br/> |OLAP データベースの 1 つまたは複数の引数が無効です。  <br/> |
|CBSOlapDatabaseReadSettingListFailed = 17021  <br/> |OLAP データベースの設定リストの読み取りに失敗しました。  <br/> |
|CBSOlapDatabaseReadSettingFailed = 17022  <br/> |OLAP データベースの設定の読み取りに失敗しました。  <br/> |
|CBSDeleteOlapDatabaseSetting = 17023  <br/> |OLAP データベースの設定の削除中にエラーが発生しました。  <br/> |
|CBSSetDefaultOlapDatabase = 17024  <br/> |既定の OLAP データベースの設定中にエラーが発生しました。  <br/> |
|CBSSetOlapDatabaseEnabled = 17025  <br/> |OLAP データベースを有効化するときにエラーが発生しました。  <br/> |
|CBSGetDefaultOlapDatabase = 17026  <br/> |既定の OLAP データベースの取得中にエラーが発生しました。  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimensionOrMeasure = 17027  <br/> |ユーザー設定フィールドをディメンションまたはメジャーとして追加することはできません。  <br/> |
|CBSOlapDatabaseAssocFieldsSettings = 17028  <br/> |OLAP データベースの関連フィールドの設定でエラーが発生しました。  <br/> |
|CBSUpdateOlapDBOperationDuplicateOrFailure = 17029  <br/> |OLAP データベースの更新処理で失敗または重複が発生しました。  <br/> |
|CBSErrorReadingDefaultDatabase = 17030  <br/> |既定の OLAP データベースの読み取り中にエラーが発生しました。  <br/> |
|CBSCreateOlapDBOperationFailure = 17031  <br/> |OLAP データベース処理の作成に失敗しました。  <br/> |
|CBSSetCubeFieldsSettingsFromListForGroupMeasureFailed = 17032  <br/> |キューブ フィールドのグループ メジャー設定リストの設定に失敗しました。  <br/> |
|CBSErrorReadingCubeDepartments = 17033  <br/> |OLAP キューブ内の部署の読み取り中にエラーが発生しました。  <br/> |
|CBSErrorMaxOlapDatabaseCountReached = 17034  <br/> |OLAP データベースの最大数に達しました。  <br/> |
|CBSErrorReadingCubeFieldsSettings = 17035  <br/> |キューブ フィールドの設定を読み取り中にエラーが発生しました。  <br/> |

<a name="pj15_ErrorCodes_CICO"></a>

## <a name="table-11-check-in-and-check-out"></a>表 11。 チェックインおよびチェック アウト

|チェックイン - エラー コードをチェック アウト|説明|
|:-----|:-----|
|CICOCheckedOutToOtherUser = 10100  <br/> |別のユーザーにチェックアウトしました。  <br/> |
|CICOAlreadyCheckedOutToYou = 10101  <br/> |既に現在のユーザーにチェックアウトしています。  <br/> |
|CICONotCheckedOut = 10102  <br/> |チェックアウトしていません。  <br/> |
|CICOCheckedOutInOtherSession = 10103  <br/> |別のセッションでチェックアウトしました。  <br/> |
|CICOInvalidSessionGuid = 10104  <br/> |セッション GUID が無効です。  <br/> |
|CICOAlreadyCheckedOutInSameSession = 10105  <br/> |同じセッションで既にチェックアウトしました。  <br/> |
|CICOCannotCheckOutVisibilityModeProjectWithMppInDocLib = 10106  <br/> |ドキュメント ライブラリに mpp ファイルがある状態で認識モード プロジェクトをチェックアウトできません。  <br/> |

<a name="pj15_ErrorCodes_CustomFields"></a>

## <a name="table-12-custom-field"></a>表 12 です。 ユーザー定義フィールド

|ユーザー設定フィールドのエラー コード|説明|
|:-----|:-----|
|CustomFieldInvalidPropertyType = 11500  <br/> |プロパティの種類が無効です。  <br/> |
|CustomFieldInvalidScope = 11503  <br/> |ユーザー設定フィールドのスコープが無効です。  <br/> |
|CustomFieldScopesMustBeIdentical = 11504  <br/> |スコープは同一である必要があります。  <br/> |
|CustomFieldInvalidEntityUID = 11505  <br/> |ユーザー設定フィールドのエンティティ GUID が無効です。  <br/> |
|CustomFieldHasInvalidPropertiesForNonLookupTableCF = 11506  <br/> |参照テーブルがないユーザー設定フィールドのプロパティが無効です。  <br/> |
|CustomFieldNonExistentWeightsTableUID = 11507  <br/> |ウェイト テーブル GUID が存在しません。  <br/> |
|CustomFieldInvalidName = 11508  <br/> |ユーザー設定フィールドの名前が無効です。  <br/> |
|CustomFieldInvalidDefault = 11510  <br/> |ユーザー設定フィールドの既定値が無効です。  <br/> |
|CustomFieldInvalidLookupTableUID = 11511  <br/> |参照テーブル GUID が無効です。  <br/> |
|CustomFieldTypeDoesNotMatchLookupTableMask = 11512  <br/> |ユーザー設定フィールドの種類が参照テーブル マスクと一致しません。  <br/> |
|CustomFieldCannotHaveNonLeafNodeDefault = 11513  <br/> |ユーザー設定フィールドの既定値は末端ノードである必要があります。  <br/> |
|CustomFieldMatchingOnlyAvailableForResources = 11514  <br/> |ユーザー設定フィールドのマッチングは、リソースにのみ使用できます。  <br/> |
|CustomFieldUIDCannotMatchLookupTableUID = 11516  <br/> |GUID が参照テーブル GUID と一致しません。  <br/> |
|CustomFieldUIDAlreadyExists = 11517  <br/> |ユーザー設定フィールド GUID が既に存在します。  <br/> |
|CustomFieldIDAlreadyExists = 11518  <br/> |ユーザー設定フィールドの識別番号が既に存在します。  <br/> |
|CustomFieldNameAlreadyExists = 11519  <br/> |ユーザー設定フィールド名が既に存在します。  <br/> |
|CustomFieldInvalidEntity = 11520  <br/> |ユーザー設定フィールドに対してエンティティが無効です。  <br/> |
|CustomFieldMaskDoesNotMatchEntityType = 11521  <br/> |コードの書式設定がエンティティの種類と一致しません。  <br/> |
|CustomFieldLowerOrderBitsOutOfRange = 11522  <br/> |下位ビットが範囲内にありません。  <br/> |
|CustomFieldInvalidMaxValues = 11523  <br/> |1 つまたは複数の最大値が無効です。  <br/> |
|CustomFieldCannotModifyCertainValuesOnceDefined = 11524  <br/> |一部の値は、定義された後は変更できません。  <br/> |
|CustomFieldNonExistentPID = 11526  <br/> |ユーザー設定フィールドのプロパティの識別番号が存在しません。  <br/> |
|CustomFieldCannotChangeBuiltInFields = 11527  <br/> |Cost Type、State、RBS などの Project Server の組み込みフィールドを変更することはできません。  <br/> |
|CustomFieldSecondaryUidCannotEqualUid = 11528  <br/> |セカンダリ GUID はプライマリ GUID に等しくなることはできません。  <br/> |
|CustomFieldCannotHaveSecondaryUIDorIDForThisEntityType = 11529  <br/> |ユーザー設定フィールドは、セカンダリ GUID、またはエンティティのこの種類の GUID を持つことができません。  <br/> |
|CustomFieldNameMatchesIntrinsicField = 11530  <br/> |ユーザー設定フィールド名が固有のフィールドに一致します。  <br/> |
|CustomFieldInvalidAggregationType = 11531  <br/> |集約の種類が無効です。  <br/> |
|CustomFieldProjectFormulaFieldsMustUseFormulaAggregation = 11532  <br/> |プロジェクト式のフィールドは式集約を使用する必要があります。  <br/> |
|CustomFieldMustSpecifyEitherIDorUID = 11700  <br/> |ユーザー設定フィールドの識別番号または GUID を指定する必要があります。  <br/> |
|CustomFieldInvalidID = 11701  <br/> |ユーザー設定フィールドの識別番号が無効です。  <br/> |
|CustomFieldInvalidUID = 11702  <br/> |ユーザー設定フィールドの GUID が無効です。  <br/> |
|CustomFieldInvalidType = 11703  <br/> |ユーザー設定フィールドの種類が無効です。  <br/> |
|CustomFieldInvalidTypeColumnFilledIn = 11704  <br/> |カスタム フィールド型の列の値が有効ではありません。 [WCF のエラー コードの例](#pj15_ErrorCodes_WCFExample)で例を参照してください。  <br/> |
|CustomFieldCodeValueDoesNotMatchLookupTable = 11706  <br/> |コードの値が参照テーブルと一致しません。  <br/> |
|CustomFieldCodeValueIsNotLeafNode = 11707  <br/> |コードの値が参照テーブルの末端ノードではありません。  <br/> |
|CustomFieldRowAlreadyExists = 11708  <br/> |ユーザー設定フィールド行が既に存在しています。  <br/> |
|CustomFieldRowDoesNotMatchCorrespondingDefinitionInDB = 11710  <br/> |ユーザー設定フィールド行がデータベース定義と一致しません。  <br/> |
|CustomFieldCodeValueAlreadyUsed = 11711  <br/> |コードの値が既に使用されています。  <br/> |
|CustomFieldMaxValuesExceeded = 11712  <br/> |ユーザー設定フィールドの最大値を超過しました。  <br/> |
|CustomFieldRequiredValueNotProvided = 11713  <br/> |必須のカスタム フィールドの値が指定されていません。 [WCF のエラー コードの例](#pj15_ErrorCodes_WCFExample)で例を参照してください。  <br/> |
|CustomFieldCannotChangeLookupTable = 11715  <br/> |ユーザー設定フィールドの参照テーブルを変更できません。  <br/> |
|CustomFieldFilterInvalid = 11716  <br/> |ユーザー設定フィールドのフィルターが無効です。  <br/> |
|CustomFieldRolldownInvalidOnFormulaFields = 11717  <br/> |式のユーザー設定フィールドでは下にスクロールできません。  <br/> |
|CustomFieldFormulaFieldCannotBeRequired = 11718  <br/> |式のフィールドを必須にすることはできません。  <br/> |
|CustomFieldFormulaFieldCannotBeWorkflowControlled = 11719  <br/> |式のフィールドをワークフローで制御することはできません。  <br/> |
|CustomFieldCannotSetValueOnFormulaFields = 11720  <br/> |式のフィールドで値を設定できません。  <br/> |
|CustomFieldNewPerRequestLimitExcedeed = 11721  <br/> |新しいユーザー設定フィールドの要求の制限を超えました。 制限は、1 つの要求の[NEW_CF_PER_REQUEST_LIMIT](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.CustomField.NEW_CF_PER_REQUEST_LIMIT.aspx)です。  <br/> |
|CustomFieldNameIsReservedName = 11722  <br/> |ユーザー設定フィールド名を予約名にすることはできません。  <br/> |
|CustomFieldNameInvalidForOlapMeasure = 11723  <br/> |OLAP キューブ メジャーに対してユーザー設定フィールド名が無効です。  <br/> |
|CustomFieldNameInvalidForOlapDimension = 11724  <br/> |OLAP キューブ ディメンションに対してユーザー設定フィールド名が無効です。  <br/> |
|CustomFieldSettingsInvalidForOlapMeasure = 11725  <br/> |OLAP キューブ メジャーに対してユーザー設定フィールドの設定が無効です。  <br/> |
|CustomFieldSettingsInvalidForOlapDimension = 11726  <br/> |OLAP キューブ ディメンションに対してユーザー設定フィールドの設定が無効です。  <br/> |
|CustomFieldCannotAddRelativeImportanceField = 11727  <br/> |相対的な重要度のフィールドを追加できません。  <br/> |
|CustomFieldCannotAddProjectImpactField = 11728  <br/> |プロジェクトの影響度のフィールドを追加できません。  <br/> |
|CustomFieldInvalidDepartmentUid = 11731  <br/> |ユーザー設定フィールドの部署 GUID が無効です。  <br/> |
|CustomFieldCannotModifyDepartmentUidOnBuiltinFields = 11732  <br/> |組み込みユーザー設定フィールドの部署 GUID は変更できません。  <br/> |
|CustomFieldCannotHaveBothLookupTableAndMultilineText = 11733  <br/> |ユーザー設定フィールドに参照テーブルと複数行テキストの両方を含めることはできません。  <br/> |
|CustomFieldCannotHaveBothFormulaAndMultilineText = 11734  <br/> |ユーザー設定フィールドに式と複数行テキストの両方を含めることはできません。  <br/> |
|CustomFieldDescriptionExceedsLimit = 11735  <br/> |カスタム フィールドの説明が長すぎます。 **MD_PROP_DESCRIPTION**プロパティの最大長は、1000 文字です。  <br/> |
|CustomFieldOnlyTextFieldsCanHaveMultilineText = 11736  <br/> |複数行テキストを格納できるのはテキストのユーザー設定フィールドのみです。  <br/> |
|CustomFieldOnlyProjectFieldsCanHaveMultilineText = 11737  <br/> |複数行テキストを格納できるのはプロジェクトのユーザー設定フィールドのみです。  <br/> |
|CustomFieldCannotChangeWorkflowControlledBehaviorForNonProjectCustomFields = 11738  <br/> |ユーザー設定フィールドは、ワークフローによって制御されている非プロジェクトのユーザー設定フィールドの動作を変更できません。  <br/> |
|CustomFieldIsWorkflowControlledAndCannotBeChanged = 11739  <br/> |このユーザー設定フィールドはワークフローによって制御されており、変更できません。  <br/> |
|CustomFieldCannotHaveRequiredFlagWhenWorkflowControlledFlagIsSet = 11740  <br/> |ユーザー設定フィールドは、ワークフローによって制御されているときは要求できません。  <br/> |
|CustomFieldFormulaCreatesCircularReference = 11742  <br/> |ユーザー設定フィールドの式が循環参照を発生させます。  <br/> |
|CustomFieldFormulaContainsInvalidFieldReference = 11743  <br/> |ユーザー設定フィールドの式に無効なフィールド参照が含まれています。  <br/> |
|CustomFieldFormulaContainsErrors = 11744  <br/> |ユーザー設定フィールドの式に 1 つ以上のエラーが含まれています。  <br/> |
|CustomFieldLocalCustomFieldNotDefined = 11745  <br/> |このローカル ユーザー設定フィールドは定義されていません。  <br/> |
|CustomFieldGraphicalIndicatorContainsErrors = 11746  <br/> |ユーザー設定フィールドのマークにエラーが含まれています。  <br/> |
|CustomFieldGraphicalIndicatorContainsInvalidFieldReference = 11747  <br/> |ユーザー設定フィールドのマークに無効なフィールド参照が含まれています。  <br/> |
|CustomFieldGraphicalIndicatorTypeMismatch = 11748  <br/> |ユーザー設定フィールドのマークに関して型の不一致が発生しています。  <br/> |
|CustomFieldFormulaFieldCannotReferenceWorkflowControlledField = 11749  <br/> |式内のフィールドは、ワークフローによって制御されているフィールドを参照できません。  <br/> |
|CustomFieldWorkflowCustomFieldBeingReferencedByFormula = 11750  <br/> |式がワークフローのユーザー設定フィールドを参照しようとしています。  <br/> |

<a name="pj15_ErrorCodes_LookupTables"></a>

## <a name="table-13-lookup-table"></a>表 13 です。 参照テーブル

|ルックアップ テーブルのエラー コード|説明|
|:-----|:-----|
|LookupTableMaskNotDefined = 11000  <br/> |参照テーブルのコードの書式設定が定義されていません。  <br/> |
|LookupTableMaskHasTooManyValues = 11001  <br/> |参照テーブルのコードの書式設定に値が多すぎます。  <br/> |
|LookupTableMaskHasGaps = 11002  <br/> |参照テーブルのコードの書式設定にギャップがあります。  <br/> |
|LookupTableMaskSequenceTypeLimitedToOneLevelDeep = 11003  <br/> |コードの書式設定のシーケンス型は 1 つのレベルに制限されています。  <br/> |
|LookupTableMaskSequenceTypeInvalid = 11004  <br/> |コードの書式設定のシーケンス型が無効です。  <br/> |
|LookupTableMaskSequenceRequiresAnyLength = 11005  <br/> |アウトライン コードには、_任意_の長さが必要です。  <br/> |
|LookupTableMaskSeparatorTooLong = 11006  <br/> |コードの書式設定の区切り文字が多すぎます。  <br/> |
|LookupTableMaskLevelMustBeBlankAcrossLCIDs = 11007  <br/> |コードの書式設定のレベルは、ロケール識別子 (言語 ID) で空白である必要があります。  <br/> |
|LookupTableMaskSeparatorInvalid = 11008  <br/> |コードの書式設定の区切り文字が無効です。  <br/> |
|LookupTableMaskBlankSeparatorInvalidAfterAnyLengthSequence = 11009  <br/> |_任意_のシーケンスの長さの後の空白の区切り文字が正しくありません。  <br/> |
|LookupTableMaskSequenceLengthInvalid = 11010  <br/> |コードの書式設定のシーケンスの長さが無効です。  <br/> |
|LookupTableMaskLevelMustBeOneOrMore = 11011  <br/> |コードの書式設定はレベル 1 以上である必要があります。  <br/> |
|LookupTableItemDoesNotFitMask = 11050  <br/> |参照テーブルのアイテムがコードの書式設定の定義と一致しません。  <br/> |
|LookupTableItemContainsSeparator = 11051  <br/> |参照テーブルのアイテムに区切り文字が含まれています。  <br/> |
|LookupTableItemFullValueTooLong = 11052  <br/> |参照テーブルのアイテムの完全な値が長すぎます。  <br/> |
|LookupTableDuplicateSiblingsDisallowed = 11053  <br/> |参照テーブルでは重複する兄弟は使用できません。  <br/> |
|LookupTableSortOrderIndexInvalid = 11054  <br/> |参照テーブルの並べ替え順序のインデックスが無効です。  <br/> |
|LookupTableSortOrderIndexDuplicate = 11055  <br/> |重複する参照テーブルの並べ替え順序のインデックス。  <br/> |
|LookupTableSortOrderTypeInvalid = 11056  <br/> |参照テーブルの並べ替え順序の種類が無効です。  <br/> |
|LookupTableSortOrderMustComeAfterParentSortOrder = 11057  <br/> |並べ替え順序は、親並べ替え順序の後に来る必要があります。  <br/> |
|LookupTableSortOrderMustComeBeforeParentNextSiblingSortOrder = 11058  <br/> |並べ替え順序は、次の兄弟並べ替え順序の親の前に来る必要があります。  <br/> |
|LookupTableInvalidCookieLength = 11060  <br/> |参照テーブルに対するクッキーの長さが無効です。  <br/> |
|LookupTableMustHaveValuesForPrimaryLCIDorJustOneValue = 11061  <br/> |参照テーブルは、プライマリ ロケール識別子 (言語 ID) の複数の値、または 1 つだけの値を持つ必要があります。たとえば、多言語参照テーブルを作成した場合、レベルごとにマスク値を 1 つのみ追加するか、まずプライマリ LCID の値を追加します。  <br/> |
|LookupTableLCIDNotSupportedInLookupTableLanguages = 11062  <br/> |ロケール識別子 (言語 ID) が参照テーブルの言語に含まれていません。  <br/> |
|LookupTableInvalidDescriptionLength = 11063  <br/> |参照テーブルのアイテムの説明の長さが無効です。  <br/> |
|LookupTableCannotChangeBuiltInTables = 11064  <br/> |組み込み参照テーブルを変更することはできません。  <br/> |
|LookupTableCannotChangeTypeOnceCreated = 11065  <br/> |参照テーブルの作成後、参照テーブルの種類を変更することはできません。  <br/> |
|LookupTableCannotDeleteLTWithDependantCustomField = 11066  <br/> |ユーザー設定フィールドで使用されている参照テーブルを削除することはできません。  <br/> |
|LookupTableAllLevelsNotFilled = 11067  <br/> |すべての参照テーブルのレベルを指定する必要があります。  <br/> |
|LookupTableDuplicateName = 11068  <br/> |参照テーブル名は一意である必要があります。  <br/> |
|LookupTableInvalidName = 11069  <br/> |参照テーブル名が無効です。  <br/> |
|LookupTableDuplicateSiblingPhoneticsDisallowed = 11071  <br/> |参照テーブルでは重複する兄弟ふりがなを使用できません。  <br/> |
|LookupTableItemInvalidLookupTable = 11073  <br/> |参照テーブルのアイテムが無効です。  <br/> |
|LookupTableInvalidPhoneticsLength = 11074  <br/> |ふりがなフィールドの長さが無効です。  <br/> |
|LookupTableAlreadyExists = 11076  <br/> |参照テーブルが既に存在します。  <br/> |
|LookupTableInvalidUID = 11078  <br/> |参照テーブル GUID が無効です。  <br/> |
|LookupTableFilterInvalid = 11079  <br/> |参照テーブルのフィルターが無効です。  <br/> |
|LookupTableLanguageParameterInvalidWithXmlFilter = 11080  <br/> |ルックアップ テーブル_xmlFilter_パラメーターを持つ言語のパラメーターが正しくありません。  <br/> |
|LookupTableInvalidParentStructUid = 11081  <br/> |参照テーブルの親構造に対して GUID が無効です。  <br/> |
|LookupTableItemContainsListSeparator = 11082  <br/> |参照テーブルのアイテムに区切り文字が含まれています。  <br/> |
   
表 14 のエラー コードには、プロジェクト詳細ページ (Pdp) の項目、Exchange の同期、Project Web App のタイムライン、およびデータベースのエラーが含まれます。 表 14 の他のエラー コードの多くは、内部的に使用されます。
  
> [!NOTE]
> Project Server 2013 では、監査のエラー コードは使用されません。 

<a name="pj15_ErrorCodes_Miscellaneous"></a>

## <a name="table-14-miscellaneous-error-codes"></a>表 14. その他のエラー コード

|その他のエラー コード|説明|
|:-----|:-----|
|AuditingUpdateFailure = 31000  <br/> |使用しません。  <br/> |
|AuditingCannotDeleteFeature = 31001  <br/> |使用しません。  <br/> |
|AuditingCannotAddFeature = 31002  <br/> |使用しません。  <br/> |
|AuditingFeatureIsNoLongerAudited = 31003  <br/> |使用しません。  <br/> |
|AuditingItemIsNotYetAvailable = 31004  <br/> |使用しません。  <br/> |
|AuditingInvalidFeatureUid = 31005  <br/> |使用しません。  <br/> |
|AuditingInvalidStoreForSelectedFeature = 31006  <br/> |使用しません。  <br/> |
|AuditingInvalidStore = 31007  <br/> |使用しません。  <br/> |
|AuditingVersionNameTooLong = 31008  <br/> |使用しません。  <br/> |
|AuditingBeginVersionFailure = 31009  <br/> |使用しません。  <br/> |
|AuditingEndVersionFailure = 31010  <br/> |使用しません。  <br/> |
|ProjectDetailPagesStrategicImpactRatingRequired = 32000  <br/> |プロジェクト詳細ページには戦略的影響評価が必要です。  <br/> |
|ProjectDetailPagesMissingPDPLinks = 32001  <br/> |プロジェクト詳細ページへのリンクがありません。  <br/> |
|ProjectDetailPagesUnavailableWorker = 32002  <br/> |プロジェクト ドリルダウンの読み込みに失敗しました。使用できるワーカーがありません。  <br/> |
|ProjectDetailPagesFailedToLoadProjectInWorker = 32003  <br/> |ワーカーの読み込みに失敗しました。  <br/> |
|AppPermissionInvalidAppPermissionId = 32300  <br/> |アプリケーション権限 ID に問題があります。  <br/> |
|InvariantValidationPSIFailed = 40000  <br/> |プライベート メソッドは、 **ValidationMethodFailed**を返す場合に、 **PWA**メソッドによって返されます。 内部で使用します。  <br/> |
|ValidationMethodFailed = 40001  <br/> |データベースの不整合を検出すると、 **PWA**のプライベート メソッドによって返されます。 内部で使用します。  <br/> |
|GeneralExchangeSyncError = 40500  <br/> |Microsoft Exchange の同期処理に関する一般的なエラーです。内部で使用されます。  <br/> |
|ExchangeSyncRootFolderCreationFailed = 40501  <br/> |Microsoft Exchange の同期処理でルート フォルダーの作成に失敗しました。  <br/> |
|ExchangeSyncTaskFolderCreationFailed = 40502  <br/> |タスク フォルダーの作成に失敗しました。  <br/> |
|ExchangeSyncCouldNotGetRootFolder = 40503  <br/> |ルート フォルダーを取得できません。  <br/> |
|ExchangeSyncCouldNotLoadTaskObject = 40504  <br/> |タスク オブジェクトを読み込めません。  <br/> |
|ExchangeSyncNewExchangeTaskCreationFailed = 40505  <br/> |Exchange の同期処理で新しいタスクの作成に失敗しました。  <br/> |
|ExchangeSyncFailedToUpdateCacheForUser = 40506  <br/> |ユーザーの Exchange 同期キャッシュの更新に失敗しました。  <br/> |
|ExchangeSyncFailedToUpdateExchangeTask = 40507  <br/> |Microsoft Exchange のタスクの更新に失敗しました。  <br/> |
|ExchangeSyncSubscriptionUpdateFailed = 40508  <br/> |Exchange 同期サブスクリプションの更新に失敗しました。  <br/> |
|ExchangeSyncEWSUrlFailed = 40509  <br/> |Microsoft Exchange Web サービスの URL が機能しません。  <br/> |
|ExchangeSyncExchangeUrlRefreshFailed = 40510  <br/> |Exchange の URL の更新に失敗しました。  <br/> |
|ExchangeSyncExchangeSubscriptionUpdateForUserFailed = 40511  <br/> |ユーザーの Exchange サブスクリプションの更新に失敗しました。  <br/> |
|ExchangeSyncGeneralProcessingFailure = 40512  <br/> |Microsoft Exchange の同期の一般的な処理に失敗しました。  <br/> |
|ExchangeSyncDeletionOfTasksInExchangeFailure = 40513  <br/> |Exchange の同期処理のタスクの削除に失敗しました。  <br/> |
|ExchangeSyncAttemptedSyncOfInvalidConfiguredResource = 40514  <br/> |同期しようとしたリソースの構成が無効です。  <br/> |
|ExchangeSyncRetrievalOfEWSUrlCausedException = 40515  <br/> |Exchange Web サービスの取得中に例外が発生しました。  <br/> |
|TimelineViewDataDoesNotExist = 42000  <br/> |Project Web App で [スケジュール] ビューのデータが存在しません。  <br/> |
|DatabaseUndefinedError = 50000  <br/> |データベースが定義されていません。  <br/> |
|DatabaseCannotInsertDuplicateKeyError = 50001  <br/> |このデータベースでは重複するキーを挿入できません。  <br/> |

<a name="pj15_ErrorCodes_Notifications"></a>

## <a name="table-15-notification"></a>表 15。 通知

|通知のエラー コード|説明|
|:-----|:-----|
|NotificationReminderUnknown = 16050  <br/> |不明なアラーム通知。  <br/> |
|NotificationReminderParentNotSubscribed = 16051  <br/> |アラーム通知の親に対するサブスクリプションがありません。  <br/> |
|NotificationReminderParentNotFound = 16052  <br/> |アラーム通知の親が見つかりません。  <br/> |
|NotificationReminderChildStillSubscribed = 16053  <br/> |通知アラームの子に対するサブスクリプションがまだ存在しています。  <br/> |
|NotificationReminderChildNotFound = 16054  <br/> |アラーム通知の子が見つかりません。  <br/> |
|NotificationEMailDeliveryFailed = 16080  <br/> |通知電子メール メッセージの配信に失敗しました。  <br/> |
|NotificationQueueMessageFailed = 16082  <br/> |通知キュー メッセージが失敗しました。  <br/> |
|NotificationXSLTTransformationError = 16084  <br/> |通知の XSLT 変換のエラー。  <br/> |
   
表 16 に示すすべてのエラー コードは、プロジェクト ポートフォリオ分析に使用するコンポーネントであるオプティマイザーのエラー コードです。

<a name="pj15_ErrorCodes_Optimizer"></a>

## <a name="table-16-optimizer-project-portfolio-analysis"></a>表 16 です。 オプティマイザー (プロジェクト ポートフォリオ分析)

|オプティマイザーのエラー コード|説明|
|:-----|:-----|
|OptimizerDepInvalidDepType = 29000  <br/> |オプティマイザー [OptimizerDependencyDataSet.OptimizerDependenciesRow](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependenciesRow.aspx)で**DEPENDENCY_TYPE**の値が正しくありません。 [Optimizer.DependencyTypes](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Optimizer.DependencyTypes.aspx)を参照してください。  <br/> |
|OptimizerDepInvalidEntityType = 29001  <br/> |エンティティの種類が正しくありません。 [エンティティ](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.Entities.aspx)のプロパティを参照してください。  <br/> |
|OptimizerDepInvalidPosition = 29003  <br/> |[位置](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsRow.POSITION.aspx)の値が有効ではありません。  <br/> |
|OptimizerDepDuplicateDependentProjects = 29004  <br/> |[OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable.aspx)では、重複するプロジェクトがあります。  <br/> |
|OptimizerDepInvalidDependency = 29005  <br/> |オプティマイザーの依存関係が無効です。  <br/> |
|OptimizerDepCircularDependency = 29006  <br/> |循環依存関係が存在します。  <br/> |
|OptimizerCannotDeleteDependency = 29007  <br/> |依存関係を削除できません。  <br/> |
|OptimizerCannotCreateDependency = 29008  <br/> |依存関係を作成できません。  <br/> |
|OptimizerCannotUpdateDependency = 29009  <br/> |依存関係を更新できません。  <br/> |
|OptimizerCannotCreateMultipleDependencies = 29010  <br/> |複数の依存関係を作成することはできません。  <br/> |
|OptimizerCannotUpdateMultipleDependencies = 29011  <br/> |複数の依存関係を更新することはできません。  <br/> |
|OptimizerEngineMatrixNotFilled = 29100  <br/> |計算をするための十分なデータがオプティマイザーにありません。  <br/> |
|OptimizerEngineCustomFieldIsNotAConstraint = 29101  <br/> |このユーザー設定フィールドはオプティマイザーのための制約ではありません。  <br/> |
|OptimizerCouldNotCalculatePrioritiesFromCustomFields = 29102  <br/> |指定されたユーザー設定フィールドから優先度を計算することができません。  <br/> |
|OptimizerEngineBinaryInfeasibleSolution = 29103  <br/> |オプティマイザーの計算結果が実行不可能な解になります。  <br/> |
|OptimizerEngineBinaryNumericalError = 29104  <br/> |オプティマイザーの計算に数値エラーがあります。  <br/> |
|OptimizerEngineBinaryTimedOut = 29105  <br/> |オプティマイザーの計算がタイムアウトしました。  <br/> |
|OptimizerEngineBinaryMaxedIterations = 29106  <br/> |オプティマイザーの計算が最大反復回数に達しました。  <br/> |
|OptimizerEngineBinarySubOptimal = 29107  <br/> |オプティマイザーの計算結果が最適ではありません。  <br/> |
|OptimizerEngineBinaryInternalError = 29108  <br/> |オプティマイザーの計算に内部エラーがあります。  <br/> |
|OptimizerInvalidRange = 29200  <br/> |オプティマイザーの日付範囲が無効です。  <br/> |
|OptimizerNonNormalizedWeights = 29201  <br/> |[AnalysisDataSet.AnalysisPriorityDataDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisPriorityDataDataTable.aspx)の**重み**の値が正規化されていません。  <br/> |
|OptimizerCannotEditPrioritization = 29300  <br/> |ドライバーの優先度設定を編集できません。  <br/> |
|OptimizerCannotDeletePrioritization = 29301  <br/> |ドライバーの優先度設定を削除できません。  <br/> |
|OptimizerCannotCreatePrioritization = 29302  <br/> |ドライバーの優先度設定を作成できません。  <br/> |
|OptimizerCannotUpdatePrioritization = 29303  <br/> |ドライバーの優先度設定を更新できません。  <br/> |
|OptimizerCannotCalculateDriverPriorities = 29304  <br/> |ドライバーの優先度を計算できません。  <br/> |
|OptimizerCannotCreateMultiplePrioritizations = 29305  <br/> |複数のドライバーの優先度設定を作成することはできません。  <br/> |
|OptimizerCannotUpdateMultiplePrioritizations = 29306  <br/> |複数のドライバーの優先度設定を更新することはできません。  <br/> |
|OptimizerDriverRelationsNotFilled = 29307  <br/> |DriverRelationsRow データが完全ではありません。  <br/> |
|OptimizerDriversNotFilled = 29308  <br/> |ソリューションのプロジェクト ドライバーに十分な情報がありません。  <br/> |
|OptimizerDriverRelationsInvalidInversedValue = 29309  <br/> |[DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx)では、逆の値があります。  <br/> |
|OptimizerCannotCreatePrioritizationUsingInactiveDrivers = 29310  <br/> |[DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx)で指定されている使用頻度の低いドライバーです。 **DRIVER1_UID**および**DRIVER2_UID**プロパティを確認します。  <br/> |
|OptimizerCannotChangePrioritizationType = 29311  <br/> |優先度設定の種類を変更できません。  <br/> |
|OptimizerCannotSpecifyPriorityValuesForCalculatedPrioritizations = 29312  <br/> |優先度が計算されている場合は、優先度の値を指定できません。  <br/> |
|OptimizerCannotNormalizePriorityValues = 29313  <br/> |優先度の値を正規化できません。  <br/> |
|OptimizerTooManyDriversInPrioritization = 29314  <br/> |優先度設定の中のビジネス ドライバーが多すぎます。  <br/> |
|OptimizerInvalidProjectImpactValue = 29400  <br/> |プロジェクトの影響度の値が無効です。  <br/> |
|OptimizerCannotDeleteDriver = 29401  <br/> |プロジェクト ドライバーを削除できません。  <br/> |
|OptimizerCannotCreateDriver = 29402  <br/> |プロジェクト ドライバーを作成できません。  <br/> |
|OptimizerCannotUpdateDriver = 29403  <br/> |プロジェクト ドライバーを更新できません。  <br/> |
|OptimizerCannotEditDriver = 29404  <br/> |プロジェクト ドライバーを編集できません。  <br/> |
|OptimizerCannotCreateMultipleDrivers = 29405  <br/> |複数のドライバーを作成することはできません。  <br/> |
|OptimizerCannotUpdateMultipleDrivers = 29406  <br/> |複数のドライバーを更新することはできません。  <br/> |
|OptimizerInvalidRelativeImportanceValue = 29407  <br/> |相対的な重要度の値が無効です。  <br/> |
|OptimizerInvalidDriverUid = 29500  <br/> |ドライバーの GUID が無効です。  <br/> |
|OptimizerInvalidEntityType = 29501  <br/> |オプティマイザーのエンティティ型が無効です。  <br/> |
|OptimizerInvalidProjectUid = 29502  <br/> |プロジェクト GUID が無効です。  <br/> |
|OptimizerInvalidCustomFieldUid = 29503  <br/> |オプティマイザーのユーザー設定フィールドの GUID が無効です。  <br/> |
|OptimizerInvalidHardConstraintUid = 29504  <br/> |厳密な制約の GUID が無効です。  <br/> |
|OptimizerInvalidAnalysisUid = 29505  <br/> |分析の GUID が無効です。  <br/> |
|OptimizerDriverFilterInvalid = 29506  <br/> |ドライバー フィルターが無効です。  <br/> |
|OptimizerPrioritizationFilterInvalid = 29507  <br/> |優先度設定フィルターが無効です。  <br/> |
|OptimizerCannotLoadOptimizationEngine = 29508  <br/> |オプティマイザーの計算エンジンを読み込めません。  <br/> |
|OptimizerAnalysisFilterInvalid = 29509  <br/> |分析フィルターが無効です。  <br/> |
|OptimizerSolutionFilterInvalid = 29510  <br/> |オプティマイザーのソリューション フィルターが無効です。  <br/> |
|OptimizerDependenciesFilterInvalid = 29511  <br/> |オプティマイザーの依存関係フィルターが無効です。  <br/> |
|OptimizerInvalidSolutionUid = 29512  <br/> |オプティマイザーのソリューション GUID が無効です。  <br/> |
|OptimizerInvalidViewUid = 29513  <br/> |オプティマイザーのビュー GUID が無効です。  <br/> |
|OptimizerInvalidAnalysisType = 29600  <br/> |ポートフォリオ分析の種類が無効です。  <br/> |
|OptimizerInvalidPrioritizationType = 29601  <br/> |オプティマイザーの優先度設定の種類が無効です。  <br/> |
|OptimizerCannotDeleteAnalysis = 29602  <br/> |ポートフォリオ分析を削除できません。  <br/> |
|OptimizerCannotCreateAnalysis = 29603  <br/> |ポートフォリオ分析を作成できません。  <br/> |
|OptimizerCannotUpdateAnalysis = 29604  <br/> |ポートフォリオ分析を更新できません。  <br/> |
|OptimizerInvalidPrioritizationUid = 29607  <br/> |優先度設定の GUID が無効です。  <br/> |
|OptimizerCannotCreateMultipleAnalyses = 29608  <br/> |複数のポートフォリオ分析を作成することはできません。  <br/> |
|OptimizerCannotUpdateMultipleAnalyses = 29609  <br/> |複数のポートフォリオ分析を更新することはできません。  <br/> |
|OptimizerCannotCalculateProjectPriorities = 29610  <br/> |オプティマイザーはプロジェクトの優先度を計算できません。  <br/> |
|OptimizerCannotDeleteAnalysisProjectImpact = 29611  <br/> |ポートフォリオ分析内のプロジェクトの影響度を削除することはできません。  <br/> |
|OptimizerCannotChangeAnalysisProjects = 29612  <br/> |ポートフォリオ分析内のプロジェクトを変更することはできません。  <br/> |
|OptimizerCannotChangePriorityData = 29613  <br/> |優先度のデータは変更できません。  <br/> |
|OptimizerCannotEditAnalysis = 29614  <br/> |ポートフォリオ分析を編集することはできません。  <br/> |
|OptimizerInvalidPlannerData = 29615  <br/> |オプティマイザーのプランナーのデータが無効です。  <br/> |
|OptimizerCannotChangeImpactData = 29616  <br/> |プロジェクトの影響度のデータは変更できません。  <br/> |
|OptimizerInvalidProjectsNumber = 29617  <br/> |プロジェクトの数が無効です。  <br/> |
|OptimizerCannotAddImpactCFUIDToCFAnalysis = 29618  <br/> |ポートフォリオ分析のためのプロジェクトへの影響ユーザー設定フィールド GUID ([PROJECT_IMPACT_CF_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.PROJECT_IMPACT_CF_UID.aspx) ) を追加することはできません。  <br/> |
|OptimizerInvalidDepartmentUid = 29619  <br/> |[DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.DEPARTMENT_UID.aspx)が有効ではありません。  <br/> |
|OptimizerTooManyProjectsInAnalysis = 29620  <br/> |分析に含まれるプロジェクトが多すぎます。  <br/> |
|QueueAnalysisCannotDeleteAnalysis = 29680  <br/> |[QueueDeleteAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteAnalyses.aspx)メソッドは、分析を削除できません。  <br/> |
|QueueAnalysisCannotCreateAnalysis = 29681  <br/> |[QueueCreateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateAnalysis.aspx)メソッドは、解析を作成できません。  <br/> |
|QueueAnalysisCannotUpdateAnalysis = 29682  <br/> |[QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx)メソッドは、分析を更新できません。  <br/> |
|AnalysisMismatchedJobList = 29690  <br/> |分析ジョブリストが一致しません。  <br/> |
|OptimizerInvalidForceInLookupTableUid = 29691  <br/> |参照テーブルの GUID を強制的に選択できません。  <br/> |
|OptimizerInvalidForceOutLookupTableUid = 29692  <br/> |参照テーブルの GUID を強制的に除外できません。  <br/> |
|OptimizerDuplicateForceLookupTableUids = 29693  <br/> |強制した参照テーブルの GUID が重複しています。  <br/> |
|OptimizerInvalidDecisionResult = 29701  <br/> |判断結果が無効です。  <br/> |
|OptimizerInvalidForcedStatus = 29702  <br/> |強制した状態が無効です。  <br/> |
|OptimizerCannotDeleteSolution = 29703  <br/> |[QueueDeleteOptimizerSolutions](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteOptimizerSolutions.aspx)メソッドでは、オプティマイザーのソリューションを削除できません。  <br/> |
|OptimizerCannotCreateSolution = 29704  <br/> |[QueueCreateOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateOptimizerSolution.aspx)メソッドを作成できません、オプティマイザーのソリューションです。  <br/> |
|OptimizerCannotUpdateSolution = 29705  <br/> |[QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx)メソッドでは、オプティマイザーのソリューションを更新できません。  <br/> |
|OptimizerCannotCalculateSolutionStrategicAlignment = 29706  <br/> |オプティマイザーは戦略的アライメントのソリューションを計算できません。  <br/> |
|OptimizerCannotCreateMultipleSolutions = 29707  <br/> |オプティマイザーは複数のソリューションを作成できません。  <br/> |
|OptimizerCannotUpdateMultipleSolutions = 29708  <br/> |オプティマイザーは複数のソリューションを更新できません。  <br/> |
|OptimizerCannotAddPrioritizationToCFAnalysis = 29709  <br/> |オプティマイザーは分析のユーザー設定フィールドに優先度設定を追加できません。  <br/> |
|OptimizerTableIsReadOnly = 29710  <br/> |オプティマイザーのテーブルは読み取り専用です。  <br/> |
|OptimizerSolutionCreateMessageFailed = 29711  <br/> |オプティマイザーは "ソリューションが作成されたました" メッセージの作成に失敗しました。  <br/> |
|OptimizerSolutionDeleteMessageFailed = 29712  <br/> |オプティマイザーは "ソリューションが削除されました" メッセージの作成に失敗しました。  <br/> |
|OptimizerCannotCalculateEfficientFrontier = 29714  <br/> |オプティマイザーは分析の有効フロンティアを計算できませんでした。  <br/> |
|OptimizerCannotUpdateSolutionProperties = 29715  <br/> |ソリューションのプロパティを更新できません。  <br/> |
|OptimizerInvalidConstraintPosition = 29716  <br/> |オプティマイザー内での制約の位置が無効です。  <br/> |
|OptimizerInvalidHardConstraintPosition = 29717  <br/> |オプティマイザー内での厳密な制約の位置が無効です。  <br/> |
|OptimizerInvalidConstraintLimit = 29718  <br/> |オプティマイザー内での制約制限値が無効です。  <br/> |
|OptimizerInvalidConstraintValue = 29719  <br/> |制約値が無効です。  <br/> |
|OptimizerInvalidSolutionProjectsSet = 29720  <br/> |ソリューション内のプロジェクト セットが無効です。  <br/> |
|OptimizerCannotCommitSolution = 29721  <br/> |[CommitOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.CommitOptimizerSolution.aspx)メソッドは、ソリューションをコミットできません。  <br/> |
|OptimizerInvalidInputData = 29723  <br/> |オプティマイザーの入力データが無効です。  <br/> |
|OptimizerInvalidConstraintSet = 29724  <br/> |オプティマイザーの制約セットが無効です。  <br/> |
|OptimizerCannotUpdateAnalysisMetrics = 29725  <br/> |分析メトリックを更新できません。  <br/> |
|OptimizerSolutionMismatchedJobList = 29726  <br/> |ソリューション内のジョブリストが一致しません。  <br/> |
|OptimizerInvalidForceLookupTableValue = 29727  <br/> |強制した参照テーブルの値が無効です。  <br/> |
|OptimizerCannotCreateSolutionWhileAnalysisUpdateIsPending = 29728  <br/> |分析の更新が承認待ちの間はオプティマイザーのソリューションを作成できません。  <br/> |
|OptimizerProjectSelectorAtLeastOne = 29800  <br/> |少なくとも 1 つのプロジェクトをオプティマイザー用に選択する必要があります。  <br/> |
   
表 17 に示すエラー コードは、プロジェクト ポートフォリオ分析に使用するコンポーネントであるプランナーのエラー コードです。

<a name="pj15_ErrorCodes_Planner"></a>

## <a name="table-17-planner-project-portfolio-analysis"></a>表 17 です。 プランナー (プロジェクト ポートフォリオ分析)

|プランナーのエラー コード|説明|
|:-----|:-----|
|PlannerSolutionMessageDeleteFailed = 28000  <br/> |キュー エラー: プランナー ソリューションを削除するためのメッセージが失敗しました。  <br/> |
|PlannerSolutionMessageCreateFailed = 28001  <br/> |キュー エラー: プランナー ソリューションを作成するためのメッセージが失敗しました。  <br/> |
|PlannerInvalidRBSValueUid = 28002  <br/> |プランナー データ内の RBS 値の GUID が無効です。  <br/> |
|PlannerInvalidCustomFieldUid = 28003  <br/> |ユーザー設定フィールドの GUID が無効です。  <br/> |
|PlannerHorizonInvalid = 28004  <br/> |プランナーの計画対象期間が無効です。計画対象期間とは、能力計画のために指定する期間です。  <br/> |
|PlannerHorizonTooBig = 28005  <br/> |対象計画期間の日付が大きすぎます。  <br/> |
|PlannerInvalidBookingType = 28006  <br/> |リソースの予約の種類が無効です。  <br/> |
|PlannerInvalidTimeScale = 28007  <br/> |タイム スケールが無効です。  <br/> |
|PlannerInvalidProjectSNET = 28008  <br/> |プロジェクトの "指定日以後に開始" の日付が無効です。  <br/> |
|PlannerInvalidProjectFNLT = 28009  <br/> |プロジェクトの "指定日までに終了" の日付が無効です。  <br/> |
|PlannerInvalidAnalysisStartDate = 28010  <br/> |プロジェクトの[開始日](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectRequirementsByRoleRow.START_DATE.aspx)が正しくありません。  <br/> |
|PlannerInvalidAnalysisDuration = 28011  <br/> |ポートフォリオ分析のための[期間](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectsRow.DURATION.aspx)が正しくありません。  <br/> |
|PlannerInvalidHorizonStartDate = 28012  <br/> |計画対象期間の開始日が無効です。  <br/> |
|PlannerInvalidHorizonEndDate = 28013  <br/> |計画対象期間の終了日が無効です。  <br/> |
|PlannerInvalidHorizonTimeScale = 28014  <br/> |計画対象期間のタイム スケールが無効です。  <br/> |
|PlannerInvalidAnalysisType = 28015  <br/> |ポートフォリオ分析の種類が無効です。  <br/> |
|PlannerHorizonStartDateDoesNotMatchTimeScale = 28016  <br/> |計画対象期間の開始日がタイム スケールに一致しません。  <br/> |
|PlannerHorizonEndDateDoesNotMatchTimeScale = 28017  <br/> |計画対象期間の終了日がタイム スケールに一致しません。  <br/> |
|PlannerAnalysisNoCapacityData = 28037  <br/> |ポートフォリオ分析のリソース最大利用可能時間データが存在しません。  <br/> |
|PlannerInvalidSolutionUid = 28100  <br/> |分析ソリューションの GUID が無効です。  <br/> |
|PlannerInvalidOptimizerSolutionUid = 28101  <br/> |オプティマイザー ソリューションの GUID が無効です。  <br/> |
|PlannerInvalidLookupTableValueUid = 28102  <br/> |参照テーブル値の GUID が無効です。  <br/> |
|PlannerInvalidEfficientFrontierUid = 28103  <br/> |[FRONTIER_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionEfficientFrontierRow.FRONTIER_UID.aspx)が有効ではありません。  <br/> |
|PlannerInvalidProjectUid = 28104  <br/> |プロジェクト GUID が無効です。  <br/> |
|PlannerInvalidAllocationThreshold = 28105  <br/> |割り当てしきい値が無効です。  <br/> |
|PlannerInvalidHiringType = 28109  <br/> |[HIRING_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.HIRING_TYPE.aspx)が有効ではありません。 [Planner.PlannerHiringType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.PlannerHiringType.aspx)を参照してください。  <br/> |
|PlannerInvalidConstraintType = 28110  <br/> |[CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_TYPE.aspx)が有効ではありません。 [Planner.ConstraintType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.ConstraintType.aspx)を参照してください。  <br/> |
|PlannerInvalidConstraintValue = 28111  <br/> |[CONSTRAINT_VALUE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_VALUE.aspx)が有効ではありません。  <br/> |
|PlannerInvalidRateTable = 28112  <br/> |[RATE_TABLE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.RATE_TABLE.aspx)が有効ではありません。  <br/> |
|PlannerInvalidSolutionForConstraint = 28113  <br/> |制約に関するプランナー ソリューションが無効です。プランナーの最初のパスで実施するプロジェクトが多すぎます。  <br/> |
|PlannerInvalidSolutionForDependencies = 28114  <br/> |ビジネスの依存関係または競合を検討するプロジェクトが多すぎるため、プランナー ソリューションは無効です。このエラーは 2 番目のパスで発生します。  <br/> |
|PlannerInvalidSolutionForScheduling = 28115  <br/> |循環依存関係が存在するため、スケジュールに関するプランナー ソリューションは無効です。  <br/> |
|PlannerInvalidAnalysisUid = 28116  <br/> |[ANALYSIS_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.ANALYSIS_UID.aspx)が有効ではありません。  <br/> |
|PlannerInvalidProjectStartDate = 28200  <br/> |プロジェクトの開始日が無効です。  <br/> |
|PlannerInvalidProjectEndDate = 28201  <br/> |プロジェクトの終了日が無効です。  <br/> |
|PlannerInvalidProjectDuration = 28202  <br/> |プロジェクト期間が無効です。  <br/> |
|PlannerInvalidProjectFNLTDate = 28203  <br/> |プロジェクトの "指定日までに終了" の日付が無効です。  <br/> |
|PlannerInvalidProjectSNETDate = 28204  <br/> |プロジェクトの "指定日以後に開始" の日付が無効です。  <br/> |
|PlannerCannotCreateSolution = 28900  <br/> |プランナーがソリューションを作成できません。  <br/> |
|PlannerCannotUpdateSolution = 28901  <br/> |プランナーがソリューションを更新できません。  <br/> |
|PlannerCannotDeleteSolution = 28902  <br/> |プランナーがソリューションを削除できません。  <br/> |
|PlannerCannotCreateMultipleSolutions = 28903  <br/> |プランナーは複数のソリューションを作成できません。  <br/> |
|PlannerCannotUpdateMultipleSolutions = 28904  <br/> |プランナーは複数のソリューションを更新できません。  <br/> |
|PlannerTableIsReadOnly = 28907  <br/> |**DataTable**は、読み取り専用です。  <br/> |
|PlannerCannotCommitSolution = 28908  <br/> |プランナーはソリューションをデータベースにコミットできません。  <br/> |
|PlannerFieldIsReadOnly = 28909  <br/> |フィールドは読み取り専用です。  <br/> |
|PlannerProjectNotInParentSolution = 28910  <br/> |プロジェクトは親ソリューションではありません。  <br/> |
|PlannerProjectNotSelectedInParentSolution = 28911  <br/> |親ソリューションの中でプロジェクトが選択されていません。  <br/> |
|PlannerProjectNotInParentAnalysis = 28912  <br/> |プロジェクトは親ポートフォリオ分析に含まれていません。  <br/> |
|PlannerProjectBeyondHorizon = 28913  <br/> |プロジェクトが計画対象期間を超えて拡張されています。  <br/> |
|PlannerResourceAllocationInternalError = 28915  <br/> |リソース割り当てに内部エラーがあります。  <br/> |
|PlannerResourceAllocationInfeasibleSolution = 28916  <br/> |リソース割り当ては実行不可能な解です。  <br/> |
|PlannerProjectEndDateViolatesDependency = 28917  <br/> |プロジェクトの終了日が依存関係に違反しています。  <br/> |
|PlannerInvalidProjectsSet = 28919  <br/> |プロジェクト セットが無効です。  <br/> |
|PlannerInvalidInputData = 28920  <br/> |プランナーの入力データが無効です。  <br/> |
|PlannerDecimalOverflowError = 28921  <br/> |プランナー内で 10 進数のオーバーフロー エラーが発生しています。  <br/> |
|PlannerSolutionMismatchedJobList = 28922  <br/> |ソリューション内に不一致のジョブ リストがあります。  <br/> |
|PlannerInvalidForceLookupTableValue = 28923  <br/> |参照テーブルの強制した値が無効です。  <br/> |
|PlannerNoHiredResource = 28924  <br/> |提案用に取得したリソースがありません。  <br/> |

<a name="pj15_ErrorCodes_Projects"></a>

## <a name="table-18-project"></a>表 18。 Project

|プロジェクトのエラー コード|説明|
|:-----|:-----|
|ProjectGlobalNotFound = 100  <br/> |エンタープライズ グローバル テンプレートが見つかりません。  <br/> |
|ProjectGlobalCannotBeDeleted = 101  <br/> |エンタープライズ グローバル テンプレートを削除できません。  <br/> |
|ProjectNotFound = 1000  <br/> |プロジェクトが見つかりません。  <br/> |
|ProjectAlreadyExists = 1001  <br/> |プロジェクトが既に存在します。  <br/> |
|ProjectCheckedoutToOtherUser = 1002  <br/> |プロジェクトが別のユーザーにチェックアウトされました。  <br/> |
|ProjectTypeInvalidForCreate = 1003  <br/> |作成操作に対してプロジェクトの種類が無効です。  <br/> |
|ProjectParametersInvalid = 1004  <br/> |1 つまたは複数のプロジェクトのパラメーターが無効です。  <br/> |
|ProjectNotCheckedoutToUser = 1006  <br/> |プロジェクトがユーザーにチェックアウトされていません。  <br/> |
|ProjectCheckedout = 1007  <br/> |プロジェクトがチェックアウトされました。  <br/> |
|ProjectTypeInvalid = 1008  <br/> |プロジェクトの種類が無効です。  <br/> |
|ProjectIDInvalid = 1009  <br/> |プロジェクトの識別番号が無効です。  <br/> |
|ProjectNameTooLong = 1014  <br/> |プロジェクト名が長すぎます。  <br/> |
|ProjectManagerNameTooLong = 1015  <br/> |プロジェクト マネージャー名が長すぎます。  <br/> |
|ProjectNameInvalid = 1016  <br/> |プロジェクト名が無効です。  <br/> |
|ProjectStartDateMissing = 1025  <br/> |プロジェクトの開始日付がありません。  <br/> |
|ProjectNameMissing = 1026  <br/> |プロジェクト名がありません。  <br/> |
|ProjectVersionMissing = 1027  <br/> |プロジェクトのバージョンがありません。  <br/> |
|ProjectDoesNotExist = 1028  <br/> |プロジェクトが存在しません。  <br/> |
|ProjectMultipleProjectsInvalid = 1029  <br/> |複数のプロジェクトが無効です。  <br/> |
|ProjectHasWriteLock = 1030  <br/> |プロジェクトはデータベースで書き込みロックを使用しています。  <br/> |
|ProjectHasPendingWriteLock = 1031  <br/> |プロジェクトは保留中の書き込みロックを使用しています。  <br/> |
|ProjectHasNoReadLock = 1032  <br/> |プロジェクトには読み込みロックがありません。  <br/> |
|ProjectHasReadLock = 1033  <br/> |プロジェクトは読み込みロックを使用しています。  <br/> |
|ProjectNameAlreadyExists = 1034  <br/> |プロジェクト名が既に存在しています。  <br/> |
|ProjectOptCriticalSlackLimitInvalid = 1035  <br/> |オプションのクリティカルな余裕期間の制限が無効です。  <br/> |
|ProjectOptCurrencyPositionInvalid = 1036  <br/> |オプションの通貨記号の位置が無効です。  <br/> |
|ProjectOptCurrencyDigitsInvalid = 1037  <br/> |オプションの通貨桁数が無効です。  <br/> |
|ProjectOptCurrencySymbolTooLong = 1038  <br/> |オプションの通貨記号が長すぎます。  <br/> |
|ProjectCannotDelete = 1039  <br/> |プロジェクトを削除できません。通常のプロジェクトまたはテンプレート サーバー側のプロジェクトのみを削除できます。  <br/> |
|ProjectCannotAdd = 1040  <br/> |サーバー側のプロジェクトで、 **AddToProject**メソッドを使用することはできません。  <br/> |
|ProjectOptCurrencySymbolInvalid = 1041  <br/> |オプションの通貨記号が無効です。  <br/> |
|ProjectHasNoWriteLock = 1042  <br/> |プロジェクトには書き込みロックがありません。  <br/> |
|ProjectFilterInvalid = 1043  <br/> |プロジェクト フィルターが無効です。  <br/> |
|ProjectTooLarge = 1044  <br/> |プロジェクトの提案が長すぎます。  <br/> |
|ProjectOptCurrencyCodeNot3Chars = 1045  <br/> |オプションの通貨コードが 3 文字ではありません。  <br/> |
|ProjectOptCurrencyCodeInvalid = 1046  <br/> |プロジェクト オプションの通貨コードが無効です。  <br/> |
|ProjectActualsAreProtected = 1047  <br/> |プロジェクトの実績は保護されています。  <br/> |
|ProjectTemplateNotFound = 1048  <br/> |プロジェクト テンプレートが見つかりません。  <br/> |
|ProjectCurrencyCodeInvalid = 1049  <br/> |通貨コードが無効です。  <br/> |
|ProjectCannotEditCostResource = 1050  <br/> |コスト リソースを編集できません。  <br/> |
|ProjectIsNotPublished = 1051  <br/> |プロジェクトが発行されていません。  <br/> |
|ProjectExceededLWPTaskLimit = 1052  <br/> |プロジェクトの提案 (ライトウェイト プロジェクト) のタスクの制限を超過しました。  <br/> |
|ProjectOptFinishDateInvalid = 1053  <br/> |プロジェクト オプションの終了日付が無効です。  <br/> |
|ProjectExceededItemsLimit = 1054  <br/> |処理するアイテムの制限を超えました。 Project Server サービス アプリケーションは、すべてのテーブルの合計が 1,000 以上の項目を追加または**ProjectDataSet**を使用できません。 1,000 以上の項目を処理するを使用して、複数の呼び出しでは、たとえば、 **QueueUpdateProject**に。  <br/> |
|ProjectColumnNotReadOnly = 1055  <br/> |列は読み取り専用ではありません。  <br/> |
|ProjectInvalidOwner = 1056  <br/> |プロジェクトの所有者が無効です。  <br/> |
|ProjectCantEditPctWrkCompForNonWrkRscs = 1057  <br/> |実際の作業の割り当てがないタスクの**PctWorkComplete**を編集することはできません。  <br/> |
|ProjectCannotEditMaterialResource = 1058  <br/> |数量単価型リソースを編集できません。  <br/> |
|ProjectCannotEditFieldWhenTaskHasNoWorkAssignment = 1059  <br/> |タスクに作業割り当てがないため、フィールドを編集できません。  <br/> |
|ProjectSubProjectNotFound = 1070  <br/> |サブプロジェクトが見つかりません。  <br/> |
|ProjectResourceNotFound = 1100  <br/> |リソースが見つかりません。  <br/> |
|ProjectResourceAlreadyExists = 1101  <br/> |リソースが既に存在します。  <br/> |
|ProjectCannotReplaceResourceWithSelf = 1106  <br/> |リソースを同じオブジェクトで置き換えることはできません。  <br/> |
|ProjectCannotChangeLockedTrackingMethod = 1107  <br/> |進捗管理方法がロックされているため、変更できません。  <br/> |
|ProjectInvalidColumnForCompatibilityMode = 1108  <br/> |互換モードの列が無効です。  <br/> |
|ProjectUpdateInvalidUpdateSequenceNumber = 1151  <br/> |プロジェクトの更新内の連番が無効です。  <br/> |
|ProjectUpdateDuplicateUpdateSequenceNumber = 1152  <br/> |プロジェクトの更新内の連番が重複しています。  <br/> |
|ProjectUpdateNullUpdateSequenceNumber = 1153  <br/> |プロジェクトの更新内の連番が null です。  <br/> |
|ProjectUpdateNullUpdateColumnNames = 1154  <br/> |プロジェクトの更新内の列名が null です。  <br/> |
|ProjectUpdateInvalidProjectUID = 1155  <br/> |プロジェクトの更新内のプロジェクト GUID が無効です。  <br/> |
|ProjectUpdateInvalidColumnForUpdate = 1156  <br/> |プロジェクトの更新の列が無効です。  <br/> |
|ProjectUpdateCannotEditColumn = 1157  <br/> |プロジェクトの更新内の列を編集できません。  <br/> |
|ProjectUpdateNoChangesToValidateAndSchedule = 1158  <br/> |プロジェクトの更新に、検証およびスケジュール設定が可能な変更が含まれていません。  <br/> |
|LinkNotFound = 1159  <br/> |リンクが見つかりません。  <br/> |
|ProjectUpdateInvalidColumnValue = 1160  <br/> |プロジェクトの更新内の列値が無効です。  <br/> |
|ProjectCannotDeleteItem = 1161  <br/> |プロジェクト アイテムを削除できません。  <br/> |
|ProjectUpdateCannotComputeOptIndex = 1162  <br/> |プロジェクトの更新内で最適化インデックスを計算できません。  <br/> |
|ProjectCannotUpdateDueToVisibilityMode = 1163  <br/> |プロジェクトが表示モードになっているため更新できません。  <br/> |
|ProjectNodeConsistencyException = 9132  <br/> |例外: ノードが矛盾しています。  <br/> |
|ProjectSchedulingEngineException = 9133  <br/> |スケジュール エンジンでの例外。  <br/> |
|ProjectFormulaCalculationException = 9134  <br/> |式の計算での例外。  <br/> |
|ProjectUpdateDatabaseException = 9135  <br/> |データベース更新での例外。  <br/> |
|ProjectDeleteException = 9136  <br/> |プロジェクトの削除での例外。  <br/> |
|ProjectOperationException = 9137  <br/> |プロジェクト操作での例外。  <br/> |
|ProjectCannotComunicateWithPCS = 9138  <br/> |PCS ワーカーとの通信に失敗しました。  <br/> |
|ProjectPCSSessionInvalid = 9139  <br/> |エンジン セッションのプロジェクトを開けませんでした。  <br/> |
|ProjectPublishFailure = 23000  <br/> |プロジェクト発行時のキューでの失敗。  <br/> |
|ProjectCurrencyConflict = 23001  <br/> |指定の通貨に競合が存在します。  <br/> |
|ProjectPublishFailed = 23002  <br/> |キューに入っている際にプロジェクトの発行が失敗しました。  <br/> |
|ProjectReversePublishFailed = 23003  <br/> |キューに入れようとしたときにプロジェクトの発行処理が失敗しました。  <br/> |
|ProjectReversePublishFailure = 23004  <br/> |キューの処理時にプロジェクトの発行を元に戻すことに失敗しました。  <br/> |
|ProjectArchiveRetentionDeleteFailure = 23005  <br/> |アーカイブ保持によりプロジェクトの削除が失敗しました。  <br/> |
|ProjectDeleteFailure = 23006  <br/> |プロジェクトの削除の失敗。  <br/> |
|ProjectPublishEnqueueFailure = 23007  <br/> |キューに入っている際のプロジェクトの発行の失敗。  <br/> |
|ProjectCheckinFailure = 23008  <br/> |キュー処理時にプロジェクトのチェックインが失敗しました。  <br/> |
|ProjectCheckinFailed = 23009  <br/> |キューに入っている際にプロジェクトのチェックインが失敗しました。  <br/> |
|ProjectCheckoutFailed = 23010  <br/> |ユーザーにはプロジェクトのチェックアウトの権限がありません。  <br/> |
|ProjectPublishSummaryEnqueueFailure = 23011  <br/> |キューに入れる際に発行サマリーが失敗しました。  <br/> |
|ProjectPublishSummaryFailed = 23012  <br/> |発行サマリーが失敗しました。  <br/> |
|ProjectUpdateScheduledProjectFailure = 26026  <br/> |キューの処理中にプロジェクトのスケジュールの更新が失敗しました。  <br/> |
|ProjectSyncProjectEnterpriseEntitiesFailure = 26033  <br/> |キューの処理中にプロジェクトのエンタープライズ エンティティの同期が失敗しました。  <br/> |
|GeneralDalDatabaseIsReadOnly = 26034  <br/> |プロジェクト ドリルダウンの読み込みに失敗しました。データベースは読み取り専用です。  <br/> |
|GeneralDatabaseCommunicationError = 26035  <br/> |ネットワークまたは認証の問題などのさまざまな原因が考えられます。  <br/> |

<a name="pj15_ErrorCodes_RDS"></a>

## <a name="table-19-reporting-data-service-rds"></a>表 19。 レポート データ サービス (RDS)

|RDS エラー コード|説明|
|:-----|:-----|
|ReportingAttributeCubeSettingsChangedMessageFailed = 24000  <br/> |キューブ設定の属性に対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingBaseCalendarChangeMessageFailed = 24001  <br/> |基本カレンダーに対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingCustomFieldMetadataChangeMessageFailed = 24002  <br/> |ユーザー設定フィールドのメタデータに対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingEntityUserViewChangedMessageFailed = 24003  <br/> |エンティティ ユーザー ビューに対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingFiscalPeriodChangeMessageFailed = 24004  <br/> |会計期間に対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingLookupTableChangeMessageFailed = 24005  <br/> |参照テーブルに対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingProjectChangeMessageFailed = 24006  <br/> |プロジェクトに対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingResourceCapacityUpdateMessageFailed = 24007  <br/> |リソース最大利用可能時間に対して RDS の更新メッセージが失敗しました。  <br/> |
|ReportingResourceChangeMessageFailed = 24008  <br/> |リソースに対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingTimesheetAdjustMessageFailed = 24009  <br/> |タイムシートに対して RDS の調整メッセージが失敗しました。  <br/> |
|ReportingTimesheetClassCreateMessageFailed = 24010  <br/> |タイムシートのクラスに対して RDS の作成メッセージが失敗しました。  <br/> |
|ReportingTimesheetDeleteMessageFailed = 24011  <br/> |タイムシートに対して RDS の削除メッセージが失敗しました。  <br/> |
|ReportingTimesheetPeriodDeleteMessageFailed = 24012  <br/> |タイムシート期間に対して RDS の削除メッセージが失敗しました。  <br/> |
|ReportingTimesheetPeriodMessageFailed = 24013  <br/> |タイムシート期間に対して RDS のメッセージが失敗しました。  <br/> |
|ReportingTimesheetSaveMessageFailed = 24014  <br/> |タイムシートに対して RDS の保存メッセージが失敗しました。  <br/> |
|ReportingTimesheetStatusChangeMessageFailed = 24015  <br/> |タイムシートの状態に対して RDS の変更メッセージが失敗しました。  <br/> |
|ReportingWSSSyncMessageFailed = 24016  <br/> |SharePoint の同期に対して RDS メッセージが失敗しました。  <br/> |
|ReportingGetSPWebFailed = 24017  <br/> |RDS は SharePoint Web の値の取得に失敗しました。  <br/> |
|ReportingWssSyncListFailed = 24018  <br/> |RDS は SharePoint リストとの同期に失敗しました。  <br/> |
|ReportingWssTransferLinksFailed = 24019  <br/> |RDS は SharePoint リンクの転送に失敗しました。  <br/> |
|ReportingQueueMessageSubmitFailed = 24020  <br/> |RDS はメッセージをキューに送信するのに失敗しました。  <br/> |
|ReportingWssSyncHRefFailed = 24021  <br/> |RDS は SharePoint HRef 値との同期に失敗しました。  <br/> |
|ReportingSyncGlobalDataMessageFailed = 24022  <br/> |エンタープライズ グローバル データと同期するための RDS のメッセージが失敗しました。  <br/> |
|ReportingRDBRefreshMessageFailed = 24023  <br/> |RDB を更新する RDS のメッセージが失敗しました。  <br/> |
|ReportingAttributeCubeDepartmentsChangedMessageFailed = 24024  <br/> |RDS メッセージは OLAP キューブの部署属性の変更に失敗しました。  <br/> |
|ReportingTimesheetProjectAggregationMessageFailed = 24025  <br/> |RDS メッセージは RDB 内のタイムシート テーブルのプロジェクトの集計に失敗しました。  <br/> |
|ReportingRdbBulkDataSyncMessageFailed = 24026  <br/> |RDS メッセージは RDB 内の一括データ同期に失敗しました。  <br/> |
|ReportingWorkflowMetadataSyncMessageFailed = 24027  <br/> |RDS メッセージはワークフローのメタデータの同期に失敗した。  <br/> |
|ReportingProjectWorkflowInformationSyncMessageFailed = 24028  <br/> |RDS メッセージはプロジェクトのワークフロー情報の同期に失敗しました。  <br/> |
|ReportingEptSyncMessageFailed = 24029  <br/> |RDS メッセージはエンタープライズ プロジェクト テンプレートの同期に失敗しました。  <br/> |
|ReportingSummaryProjectPublishMessageFailed = 24030  <br/> |RDS メッセージはサマリー プロジェクトの発行に失敗しました。  <br/> |
|ReportingSolutionCommitedDecisionChangedMessageFailed = 24031  <br/> |RDS メッセージはソリューションのコミットされた決定事項の変更に失敗しました。  <br/> |
|ReportingDelayedUpgradeFailed = 24032  <br/> |RDB の遅延したアップグレードが失敗しました。  <br/> |

<a name="pj15_ErrorCodes_Resources"></a>

## <a name="table-20-resource"></a>表 20 です。 リソース

|リソースのエラー コード|説明|
|:-----|:-----|
|ResourceNotFound = 2000  <br/> |リソースが見つかりません。  <br/> |
|ResourceAlreadyExists = 2001  <br/> |リソースが既に存在します。  <br/> |
|ResourceCheckedoutToOtherUser = 2002  <br/> |リソースが別のユーザーにチェックアウトしました。  <br/> |
|ResourceUIDInvalid = 2011  <br/> |リソース GUID が無効です。  <br/> |
|ResourceNameInvalid = 2016  <br/> |リソース名が無効です。  <br/> |
|ResourceNameTooLong = 2017  <br/> |リソース名が長すぎます。  <br/> |
|ResourceInitialsTooLong = 2018  <br/> |リソースの頭文字が長すぎます。  <br/> |
|ResourceCheckedout = 2025  <br/> |リソースがチェックアウトされています。  <br/> |
|ResourceNTAccountInvalid = 2026  <br/> |リソース Windows (NTLM) アカウントが無効です。  <br/> |
|ResourceNameAlreadyInUse = 2027  <br/> |リソース名は既に使用されています。名前は一意である必要があります。  <br/> |
|ResourceNTAccountAlreadyInUse = 2028  <br/> |リソース NTLM アカウントは既に使用されています。  <br/> |
|ResourceAdGuidAlreadyInUse = 2029  <br/> |リソース GUID は既に使用されています。  <br/> |
|ResourceHasActuals = 2031  <br/> |リソースには実績があります。  <br/> |
|ResourceNTAccountTooLong = 2035  <br/> |NTLM アカウントが長すぎます。  <br/> |
|ResourceEMailAddressTooLong = 2036  <br/> |リソースの電子メール アドレスが長すぎます。  <br/> |
|ResourceCodeTooLong = 2037  <br/> |リソースのコードが長すぎます。  <br/> |
|ResourceGroupTooLong = 2038  <br/> |リソース グループが長すぎます。  <br/> |
|ResourceWorkGroupInvalid = 2039  <br/> |リソース ワークグループが無効です。  <br/> |
|ResourceTypeInvalid = 2040  <br/> |リソースの種類が無効です。  <br/> |
|ResourceNonWorkResourceWithEMailInvalid = 2044  <br/> |非稼働日のリソースには電子メール アドレスを使用できません。  <br/> |
|rsResourceNameHasTrailingOrLeadingWhitespace = 2046  <br/> |リソース名には先頭または末尾の空白があります。  <br/> |
|ResourceCannotDeleteCallingUserAccount = 2047  <br/> |ユーザーは自分自身のアカウントを削除できません。  <br/> |
|ResourceInitialsInvalid = 2048  <br/> |リソースの頭文字が無効です。  <br/> |
|ResourceAccrueAtInvalid = 2049  <br/> |コストに計上する値が無効です。  <br/> |
|ResourceNonMaterialResourceCannotHaveMaterialLabel = 2050  <br/> |数量単価型でないリソースに数量単価型の単位を設定することはできません。  <br/> |
|ResourceMaterialResourceCannotHaveCertainFields = 2051  <br/> |数量単価型リソースには特定のフィールドを含めることはできません。  <br/> |
|ResourceAvailFromAvailToOverlap = 2052  <br/> |利用可能期間の開始日と利用可能期間の終了日が重なっています。  <br/> |
|ResourceInvalidEmailLanguage = 2053  <br/> |電子メールの言語が無効です。  <br/> |
|ResourceBookingTypeInvalid = 2055  <br/> |予約の種類が無効です。  <br/> |
|ResourceCannotReplaceMaterialResourceWithNonMaterialResource = 2056  <br/> |数量単価型のリソースを数量単価型でないリソースで置き換えることはできません。  <br/> |
|ResourceCannotUpdateEnterpriseResource = 2057  <br/> |エンタープライズ リソースを更新できません。  <br/> |
|rsResourceCannotAddLocalWithSameNameAsEnterprise = 2058  <br/> |同じ名前を持つローカル リソースをエンタープライズ リソースとして追加することはできません。  <br/> |
|ResourceCannotSetRateOnCostResource = 2059  <br/> |コスト リソースに単価を設定できません。  <br/> |
|ResourceCannotSetRateOnMaterialResource = 2060  <br/> |数量単価型リソースに単価を設定できません。  <br/> |
|ResourceCannotSetCanLevelOnNonWorkResource = 2061  <br/> |時間単価型以外のリソースにはレベルを設定できません。  <br/> |
|ResourceCannotDeleteThisUser = 2062  <br/> |このユーザーを削除できません。  <br/> |
|ResourceCannotDeactivateSelf = 2063  <br/> |リソースはそれ自体を非アクティブ化することはできません。  <br/> |
|ResourceAvailabilityDateRangesOverlap = 2064  <br/> |リソースの利用可能時間の日付範囲が重なっています。  <br/> |
|ResourceAvailabilityOutsideTheHireAndTerminationDateRange = 2065  <br/> |リソースの利用可能時間の日付が雇用開始日および雇用終了日の範囲外にあります。  <br/> |
|ResourceFilterInvalid = 2066  <br/> |リソースのフィルターが無効です。  <br/> |
|ResourceSegmentWithThisEffectiveDateDoesNotExist = 2067  <br/> |保存されていないリソース単価を削除することはできません。  <br/> |
|ResourceSegmentWithThisEffectiveDateAlready = 2068  <br/> |この有効な日付を持つセグメントが既に存在します。  <br/> |
|ResourceUserHasItemCheckedOutToItStill = 2069  <br/> |ユーザーにはまだチェックアウトされているアイテムがあります。  <br/> |
|ResourceInvalidHireDate = 2070  <br/> |雇用開始日が無効です。  <br/> |
|ResourceInvalidTerminationDate = 2071  <br/> |雇用終了日が無効です。  <br/> |
|ResourceCannotChangeExistingResourceType = 2072  <br/> |リソースの種類を変更できません。  <br/> |
|ResourceCannotSetTimesheetManagerOnSpecifiedResource = 2073  <br/> |指定されたリソースにタイムシート管理者を設定できません。  <br/> |
|ResourceInvalidTimesheetManager = 2074  <br/> |タイムシート管理者が無効です。  <br/> |
|ResourceInvalidAssignmentOwner = 2075  <br/> |割り当て所有者が無効です。  <br/> |
|ResourceCannotCreateCostResource = 2076  <br/> |コスト リソースを作成できません。  <br/> |
|ResourceInvalidRbsValue = 2077  <br/> |RBS 値が無効です。  <br/> |
|ResourceCannotSetAssignmentOwnerOnSpecifiedResource = 2078  <br/> |指定されたリソースに割り当て所有者を設定できません。  <br/> |
|ResourceFieldsInvalidForBudget = 2079  <br/> |予算に対応する 1 つまたは複数のフィールドが無効です。  <br/> |
|ResourceHyperlinkInvalid = 2080  <br/> |リソースのハイパーリンクが無効です。  <br/> |
|ResourceAuthorizationValidOnlyOnWorkResources = 2081  <br/> |承認は時間単価型リソースに対してのみ有効です。  <br/> |
|ResourceIsProjectOwner = 2082  <br/> |リソースがプロジェクトの所有者なので、リソースを削除できません。  <br/> |
|ResourceIsTimesheetManager = 2083  <br/> |リソースがタイムシート管理者なので、リソースを削除できません。  <br/> |
|ResourceIsDefaultAssignmentOwner = 2084  <br/> |リソースが既定の割り当て所有者なので、リソースを削除できません。  <br/> |
|ResourceIsAssignmentOwner = 2085  <br/> |リソースが割り当て所有者なので、リソースを削除できません。  <br/> |
|ResourceIsUsedInResourcePlan = 2086  <br/> |リソースがリソース計画で使用されているため、リソースを削除できません。  <br/> |
|ResourceCannotDeleteEnterpriseResource = 2087  <br/> |不明な理由によりエンタープライズ リソースを削除できません。  <br/> |
|ResourceSetResourceAuthorizationFailed = 2088  <br/> |リソース承認の設定に失敗しました。  <br/> |
|ResourceTooManyResourcesSpecifiedToDelete = 2089  <br/> |指定された数のリソースを削除できません。  <br/> |
|ResourceTooManyResourcesReturned = 2090  <br/> |メソッドはその数のリソースを処理できません。  <br/> |
|ResourceCannotDeleteWorkflowProxyUser = 2091  <br/> |ワークフロー プロキシ ユーザーを削除できません。  <br/> |
|ResourceInvalidEmailWithExchangeSync = 2092  <br/> |Microsoft Exchange Server との同期に関する電子メールが無効です。  <br/> |
|ResourceInvalidResourceTypeWithExchangeSync = 2093  <br/> |Exchange Server との同期に関するリソースの種類が無効です。  <br/> |
|ResourceInvalidPrincipalNameWithExchangeSync = 2094  <br/> |Exchange Server との同期に関するリソースのプリンシパル名が無効です。  <br/> |
|ResourceInvalidAuthenticationTypeWithExchangeSync = 2095  <br/> |Exchange Server との同期に関するリソースの認証の種類が無効です。  <br/> |
|ResourceExchangeSyncFlagAndPrincipalNameMismatch = 2096  <br/> |Exchange Server の同期フラグとリソースのプリンシパル名の間に不一致があります。  <br/> |
|ResourceUnsupportedUserUpdateInSharePointSecurityMode = 2097  <br/> |ユーザーの作成は SharePoint セキュリティ モードではサポートされません。  <br/> |

<a name="pj15_ErrorCodes_ResourcePlans"></a>

## <a name="table-21-resource-plan"></a>表 21 です。 リソース計画

|リソース計画のエラー コード|説明|
|:-----|:-----|
|ResourcePlanProjectPublishIncomplete = 30000  <br/> |リソース計画のプロジェクトの発行が完了していません。  <br/> |
|ResourcePlanInvalidResourceType = 30001  <br/> |リソース計画のリソースの種類が無効です。  <br/> |
|ResourcePlanInactiveResourcesDisallowed = 30002  <br/> |アクティブではないリソースは、リソース計画では使用できません。  <br/> |
|ResourcePlanFilterInvalid = 30003  <br/> |リソース計画フィルターが無効です。  <br/> |
|ResourcePlanSaveFailure = 30004  <br/> |リソース計画の保存に失敗しました。  <br/> |
|ResourcePlanCheckinFailure = 30005  <br/> |リソース計画のチェックインに失敗しました。  <br/> |
|ResourcePlanDeleteFailure = 30006  <br/> |リソース計画の削除に失敗しました。  <br/> |
|ResourcePlanInvalidUtilizationType = 30007  <br/> |リソース計画利用の種類が無効です。  <br/> |
|ResourcePlanInvalidTimescale = 30008  <br/> |リソース計画タイムスケールが無効です。  <br/> |
|ResourcePlanMismatchedJobList = 30009  <br/> |リソース計画のジョブ リストの不一致。  <br/> |
|ResourcePlanAlreadyExists = 30010  <br/> |リソース計画が既に存在します。  <br/> |
|ResourcePlanInvalidProjectUID = 30011  <br/> |リソース計画のプロジェクト GUID が無効です。  <br/> |
|ResourcePlanResourceAlreadyExists = 30012  <br/> |リソース計画には既にリソースが存在します。  <br/> |
   
表 22 のエラー コードは、**ルール**内のメソッド、 **PWA** web サービスです。 内部的に使用されます。 

<a name="pj15_ErrorCodes_Rules"></a>

## <a name="table-22-rules"></a>表 22。 ルール

|規則のエラー コード|説明|
|:-----|:-----|
|RulesNameTooLong = 21001  <br/> |承認規則の名前が長すぎます。 Project Web App にのみ内部で使用します。  <br/> |
|RulesDescriptionTooLong = 21002  <br/> |仕訳ルールの説明が長すぎます。 Project Web App にのみ内部で使用します。  <br/> |
|RulesInvalidRuleType = 21003  <br/> |ルールの種類が正しくありません。 Project Web App にのみ内部で使用します。  <br/> |
|RulesInvalidConditionType = 21004  <br/> |ルールの条件の種類が正しくありません。 Project Web App にのみ内部で使用します。  <br/> |
|RulesInvalidOperatorType = 21005  <br/> |規則の演算子の種類が正しくありません。 Project Web App にのみ内部で使用します。  <br/> |
|RulesInvalidListItemType = 21007  <br/> |ルールの一覧の項目の種類が正しくありません。 Project Web App にのみ内部で使用します。  <br/> |
|RulesNameInvalidCharacters = 21008  <br/> |無効なルールの名前の 1 つまたは複数の文字があります。 Project Web App にのみ内部で使用します。  <br/> |
|RulesDescriptionInvalidCharacters = 21009  <br/> |無効な仕訳ルールの説明の 1 つまたは複数の文字があります。 Project Web App にのみ内部で使用します。  <br/> |
|RulesInvalidValueType = 21010  <br/> |ルール内の値の型が正しくありません。 Project Web App にのみ内部で使用します。  <br/> |

<a name="pj15_ErrorCodes_Security"></a>

## <a name="table-23-security"></a>表 23 です。 セキュリティ

|セキュリティ エラー コード|説明|
|:-----|:-----|
|SecurityGroupCouldNotBeCreated = 19001  <br/> |セキュリティ グループを作成できません。  <br/> |
|SecurityFieldAccessIDInvalid = 19003  <br/> |セキュリティ フィールド アクセス コードの識別番号が無効です。  <br/> |
|SecurityCannotUpdateFacForNonExistentCategory = 19004  <br/> |セキュリティ カテゴリが存在しません。フィールド アクセス コードを更新できません。  <br/> |
|SecurityDuplicateCategoryUid = 19005  <br/> |重複するセキュリティ カテゴリ GUID。  <br/> |
|SecurityDuplicateGroupUid = 19006  <br/> |重複するセキュリティ グループ GUID。  <br/> |
|SecurityDuplicateTemplateUid = 19007  <br/> |重複するセキュリティ テンプレート GUID。  <br/> |
|SecurityInvalidTemplateUidRef = 19008  <br/> |セキュリティ テンプレート GUID が無効です。  <br/> |
|SecurityInvalidGlobalPermission = 19009  <br/> |グローバル セキュリティ権限が無効です。  <br/> |
|SecurityInvalidCategoryPermission = 19010  <br/> |セキュリティ カテゴリ権限が無効です。  <br/> |
|SecurityUpdatedGroupNotFound = 19013  <br/> |更新されたセキュリティ グループが見つかりません。  <br/> |
|SecurityUpdatedCategoryNotFound = 19014  <br/> |更新されたセキュリティ カテゴリが見つかりません。  <br/> |
|SecurityUpdatedTemplateNotFound = 19015  <br/> |更新されたセキュリティ テンプレートが見つかりません。  <br/> |
|SecurityGroupMemberNotFound = 19016  <br/> |セキュリティ グループのメンバーが見つかりません。  <br/> |
|SecurityUserNotFound = 19018  <br/> |Project Server ユーザーが見つかりません。  <br/> |
|SecurityNoCategoryRelationForPermission = 19019  <br/> |権限に対してセキュリティ カテゴリ関係が見つかりません。  <br/> |
|SecurityCannotDeleteDefaultGroup = 19020  <br/> |既定のセキュリティ グループを削除することはできません。  <br/> |
|SecurityCannotDeleteDefaultCategory = 19021  <br/> |既定のセキュリティ カテゴリを削除することはできません。  <br/> |
|SecurityCategoryCouldNotBeCreated = 19022  <br/> |セキュリティ カテゴリを作成できません。  <br/> |
|SecurityNoCategoryForPermission = 19023  <br/> |権限に対してセキュリティ カテゴリが見つかりません。  <br/> |
|SecurityNoCategoryForObject = 19024  <br/> |オブジェクトに対してセキュリティ カテゴリが見つかりません。  <br/> |
|SecurityNoCategoryForRule = 19025  <br/> |規則に対してセキュリティ カテゴリが見つかりません。  <br/> |
|SecurityNoGroupForPermission = 19026  <br/> |権限に対してセキュリティ グループが見つかりません。  <br/> |
|SecurityCannotSetPermissionForFieldGroup = 19027  <br/> |セキュリティ グループ フィールドに対して権限を設定できません。  <br/> |
|SecurityInvalidFieldGroup = 19028  <br/> |セキュリティ グループ フィールドが無効です。  <br/> |
|SecurityCannotSetOrgPermission = 19029  <br/> |セキュリティ組織の権限を設定できません。  <br/> |
|SecurityInvalidOrgPermission = 19030  <br/> |セキュリティ組織の権限が無効です。  <br/> |
|SecurityInvalidSecurityRule = 19031  <br/> |セキュリティ規則が無効です。  <br/> |
|SecurityTemplateNotFound = 19034  <br/> |セキュリティ テンプレートが見つかりません。  <br/> |
|SecurityInvalidObjectType = 19035  <br/> |セキュリティ オブジェクトの種類が無効です。  <br/> |
|SecurityDuplicateUid = 19036  <br/> |セキュリティ オブジェクト GUID が重複しています。  <br/> |
|SecurityObjectNotFound = 19037  <br/> |セキュリティ オブジェクトが見つかりません。  <br/> |
|SecurityInvalidCategoryUidRef = 19080  <br/> |セキュリティ カテゴリ GUID が無効です。  <br/> |
|SecurityInvalidProjectUidRef = 19081  <br/> |セキュリティ オブジェクトのプロジェクト GUID が無効です。  <br/> |
|SecurityInvalidGroupUidRef = 19082  <br/> |セキュリティ グループ GUID が無効です。  <br/> |
|SecurityInvalidUserUidRef = 19083  <br/> |セキュリティ オブジェクトのユーザー GUID が無効です。  <br/> |
|SecurityInvalidCategoryPermissionUidRef = 19084  <br/> |セキュリティ カテゴリの権限 GUID が無効です。  <br/> |
|SecurityInvalidGlobalPermissionUidRef = 19085  <br/> |セキュリティ グローバル アクセス権 GUID が無効です。  <br/> |
|SecurityInvalidResourceUidRef = 19086  <br/> |セキュリティ オブジェクトのリソース GUID が無効です。  <br/> |
|SecurityDeleteNotSupportedBySetMethod = 19087  <br/> |メソッドはセキュリティ オブジェクトを削除することができません。  <br/> |
|SecurityInvalidProjectCategoryPermissionUidRef = 19088  <br/> |プロジェクトのカテゴリ権限の GUID が無効です。  <br/> |
|SecurityCannotModifyCoreProjectCategoryDataInUpdate = 19089  <br/> |セキュリティ更新メソッドはコア プロジェクトのカテゴリ データを変更できません。  <br/> |
|SecurityProjectCategoryEntitiesDoNotAllowInPlaceChanges = 19090  <br/> |セキュリティ カテゴリ エンティティは更新内で変更できません。  <br/> |
|SecurityCategoryCannotAddRelationForDeletedCategory = 19091  <br/> |削除されたセキュリティ カテゴリに関するリレーションシップは追加できません。  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedCategory = 19092  <br/> |削除されたセキュリティ カテゴリに関する権限は追加できません。  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedRelation = 19093  <br/> |削除されたセキュリティ カテゴリのリレーションシップに関する権限は追加できません。  <br/> |
|SecurityCategoryCannotDeleteRelationForNewlyAddedCategory = 19094  <br/> |新たに追加されたセキュリティ カテゴリに関するリレーションシップは削除できません。  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedCategory = 19095  <br/> |新たに追加されたセキュリティ カテゴリに関する権限は削除できません。  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedRelation = 19096  <br/> |セキュリティ カテゴリ内で新たに追加されたリレーションシップに関する権限は削除できません。  <br/> |
|SecurityCategoryCannotHaveDuplicateUserOrGroupUidsForRelation = 19097  <br/> |セキュリティ カテゴリのリレーションシップに関するユーザーまたはグループの UID を重複させることはできません。  <br/> |
|SecurityCategoryPermissionMustHaveMatchingRelation = 19098  <br/> |カテゴリ権限は、一致するセキュリティ カテゴリのリレーションシップを持たなければなりません。  <br/> |
|SecurityCategoryProjectAlreadyHasSecurityProjectCategory = 19099  <br/> |選択したカテゴリの一覧には、既にプロジェクト セキュリティ カテゴリがあります。  <br/> |

<a name="pj15_ErrorCodes_Events"></a>

## <a name="table-24-project-server-event"></a>表 24 です。 プロジェクトのサーバーのイベント

|プロジェクトのサーバー イベントのエラー コード|説明|
|:-----|:-----|
|ServerEventInvalidEventId = 19033  <br/> |Project Server イベントの識別番号が無効です。  <br/> |
|ServerEventServiceNotFound = 22003  <br/> |Project Server イベント サービスが見つかりません。このエラーは Project Server のコードでは使用されませんが、生の統合ログ サービス (ULS) イベントにマッピングされます。  <br/> |
|ServerEventRemoteCouldNotReachProxy = 22005  <br/> |リモート Project Web App は、Project Server のイベント マネージャーのプロキシに到達できませんでした。 このエラーは、Project Server のコードでは使用されませんが、生 ULS イベントにマップします。  <br/> |
|ServerEventManagerCouldNotReachRemote = 22006  <br/> |Project Server のイベント マネージャーは、リモートの Project Web App に到達できませんでした。 このエラーは、Project Server のコードでは使用されませんが、生 ULS イベントにマップします。  <br/> |
|ServerEventHandlerNotSigned = 22007  <br/> |Project Server イベント ハンドラーが署名されていません。  <br/> |
|ServerEventHandlerMalformedAssemblyName = 22008  <br/> |Project Server イベント ハンドラーに対してアセンブリ名が無効です。  <br/> |
|ServerEventHandlerOrderInvalid = 22009  <br/> |Project Server イベント ハンドラーに対して命令が無効です。  <br/> |
|ServerEventHandlerDuplicateEntry = 22010  <br/> |Project Server イベント ハンドラーの重複するエントリ。  <br/> |
|ServerEventHandlerNotFound = 22011  <br/> |Project Server イベント ハンドラーが見つかりません。  <br/> |
|ServerEventHandlerDuplicateName = 22012  <br/> |Project Server イベント ハンドラーの重複する名前。  <br/> |
|ServerEventHandlerNullAssemblyNameAndEndpointUrl = 22013  <br/> |エンドポイントの URL かアセンブリ名のいずれかがあることを確認してください。  <br/> |

<a name="pj15_ErrorCodes_Statusing"></a>

## <a name="table-25-statusing-web-service"></a>表 25 です。 状態管理 web サービス 

|状態管理 web サービスのエラー コード|説明|
|:-----|:-----|
|StatusingInvalidEntity = 3102  <br/> |**状態管理**のエンティティを使用することはできません。  <br/> |
|StatusingGetDataForTaskFailed = 3103  <br/> |タスクの状態に関するデータの取得に失敗しました。  <br/> |
|StatusingGetTaskOrAssnCntrFailed = 3104  <br/> |状態のタスクまたは Assignment Center の取得に失敗しました。  <br/> |
|StatusingInvalidPIDForProjCntr = 3105  <br/> |プロジェクト センターの**状態管理**プロパティの id 番号が正しくありません。  <br/> |
|StatusingDeleteAssnFailed = 3106  <br/> |**状態管理**のプロセスで割り当てを削除できませんでした。  <br/> |
|StatusingAssnSaveFailed = 3107  <br/> |**状態管理**のプロセスに割り当てを保存できませんでした。  <br/> |
|StatusingTaskSaveFailed = 3108  <br/> |**状態管理**のプロセスのタスクを保存できませんでした。  <br/> |
|StatusingInvalidPID = 3109  <br/> |**状態管理**プロパティの id 番号が正しくありません。  <br/> |
|StatusingSetDataValueInvalid = 3111  <br/> |**状態管理**データの値が有効ではありません。  <br/> |
|StatusingSetDataFailed = 3112  <br/> |**状態管理**データの値を設定できませんでした。  <br/> |
|StatusingInvalidDelegationStart = 3113  <br/> |**DelegateAssignments**メソッドで割り当ての開始時刻が正しくありません。  <br/> |
|StatusingApprovalUpdateFailed = 3114  <br/> |状態の承認の更新に失敗しました。  <br/> |
|StatusingInvalidApprovalType = 3115  <br/> |状態の承認の種類が無効です。  <br/> |
|StatusingInternalError = 3116  <br/> |**状態管理**の方法で内部処理エラーが発生しました。  <br/> |
|StatusingInvalidUpdateData = 3117  <br/> |**状態管理**の方法でデータの更新が有効ではありません。  <br/> |
|StatusingProjectUpdateFailed = 3118  <br/> |プロジェクトの**状態管理**の更新に失敗しました。  <br/> |
|StatusingInvalidPreviewData = 3119  <br/> |**状態管理**データのプレビューが正しくありません。  <br/> |
|StatusingInvalidTransaction = 3120  <br/> |**状態管理**のトランザクションが有効ではありません。  <br/> |
|StatusingTooManyResults = 3121  <br/> |結果が多すぎます。時間配分状態データを読み込む際に 5000 を超える行が返されます。  <br/> |
|StatusingInvalidInterval = 3122  <br/> |**状態管理**メソッドの間隔が正しくありません。 間隔は分以内にする必要があり、0 より大きい必要があります。  <br/> |
|StatusingApplyUpdatesFailed = 3123  <br/> |適用に失敗した最新の**状態管理**エンキュー要求します。  <br/> |
|StatusingApplyUpdatesFailure = 3124  <br/> |キューの処理中に**状態管理**の更新プログラムを適用できませんでした。  <br/> |
|StatusingInvalidWorkData = 3125  <br/> |**状態管理**の作業データが有効ではありません。  <br/> |
|StatusingMissingNameAttribute = 3126  <br/> |**状態管理**の名前属性がありません。  <br/> |
|StatusingInvalidNameAttribute = 3127  <br/> |**状態管理**の [名前] 属性が有効ではありません。  <br/> |
|StatusingInvalidData = 3128  <br/> |**状態管理**データが有効ではありません。  <br/> |
|StatusingInvalidChangelist = 3130  <br/> |**UpdateStatus**メソッドの_changexml_パラメーターに XML データが正しくありません。  <br/> |
|StatusingInsufficientAssignmentRights = 3131  <br/> |**SetAssignmentWorkData**は、ユーザーにアクセス許可があるないために、割り当てを更新できません。  <br/> |
|StatusingInvalidChangeNumber = 3132  <br/> |**状態管理**の変更番号が正しくありません。  <br/> |
|StatusingPidNotEditable = 3133  <br/> |**状態管理**プロパティの id 番号が編集可能ではありません。  <br/> |
|StatusingCannotSetTimephasedDataInManualTasks = 3134  <br/> |**状態管理**の手動タスクのタイム スケール領域のデータを設定できません。  <br/> |
|StatusingCannotChangeTaskMode = 3135  <br/> |**状態管理**のタスク モードを変更することはできません。  <br/> |
   
**PWA** web サービスの**StatusReports**メソッドは、表 26 のエラー コードです。 Project Web App で内部的に使用されます。 

<a name="pj15_ErrorCodes_StatusReports"></a>

## <a name="table-26-statusreports"></a>表 26 です。 StatusReports 

|ステータス レポートのエラー コード|説明|
|:-----|:-----|
|StatusReportsUnknownError = 12100  <br/> |**StatusReports**で不明なエラーが発生しました。  <br/> |
|StatusReportsPeriodUnmatched = 12101  <br/> |進捗レポート期間を一致させることができません。  <br/> |
|StatusReportsPeriodUnavailable = 12102  <br/> |進捗レポート期間が利用できません。  <br/> |
|StatusReportsInvalidFormInput = 12103  <br/> |進捗レポート フォーム内のデータが無効です。  <br/> |

<a name="pj15_ErrorCodes_Tasks"></a>

## <a name="table-27-task"></a>表 27 になります。 タスク 

|タスクのエラー コード|説明|
|:-----|:-----|
|TaskIDInvalid = 7001  <br/> |タスク GUID が無効です。  <br/> |
|TaskNameTooLong = 7003  <br/> |タスク名が長すぎます。  <br/> |
|TaskTypeInvalid = 7005  <br/> |タスクの種類が無効です。  <br/> |
|TaskPriorityInvalid = 7006  <br/> |タスクの優先度が無効です。  <br/> |
|TaskConstraintTypeInvalid = 7007  <br/> |タスクの制約の種類が無効です。  <br/> |
|TaskNameInvalid = 7008  <br/> |タスク名が無効です。  <br/> |
|TaskConstraintTypeRequiresConstraint = 7010  <br/> |タスクには制約の種類が必要です。  <br/> |
|TaskConstraintTypeCannotHaveConstraintDate = 7011  <br/> |その制約の種類に対して制約の日付は使用できません。  <br/> |
|TaskSummaryTaskCannotBeMilestone = 7013  <br/> |サマリー タスクをマイルストーンにすることはできません。  <br/> |
|TaskFixedCostAccrualInvalid = 7014  <br/> |タスクに対して固定コスト計上が無効です。  <br/> |
|TaskPercentCompleteInvalid = 7015  <br/> |タスクの達成率の値が無効です。  <br/> |
|TaskWorkPercentCompleteInvalid = 7016  <br/> |タスク作業の達成率の値が無効です。  <br/> |
|TaskPhysicalPercentCompleteInvalid = 7017  <br/> |タスクの実際の達成率の値が無効です。  <br/> |
|TaskLinkTypeInvalid = 7018  <br/> |タスクのリンクの種類が無効です。  <br/> |
|TaskAlreadyExists = 7019  <br/> |タスクが既に存在します。  <br/> |
|TaskLinkAlreadyExists = 7020  <br/> |タスクのリンクが既に存在します。  <br/> |
|TaskNotFound = 7021  <br/> |タスクが見つかりません。  <br/> |
|TaskLinkNotFound = 7022  <br/> |タスクのリンクが見つかりません。  <br/> |
|TaskLinkLagInvalid = 7023  <br/> |タスクのリンクに対してラグ タイムが無効です。  <br/> |
|TaskUnableToInsert = 7025  <br/> |タスクを挿入できません。  <br/> |
|TaskAddPositionInvalid = 7026  <br/> |タスクに対する追加位置が無効です。  <br/> |
|TaskOutlineLevelInvalid = 7027  <br/> |タスク アウトライン レベルが無効です。  <br/> |
|TaskDurationFormatInvalid = 7028  <br/> |タスク期間の形式が無効です。  <br/> |
|TaskCannotAddWhereSpecified = 7029  <br/> |指定された場所にタスクを追加できません。  <br/> |
|TaskEarnedValueMethodInvalid = 7030  <br/> |タスクの達成額の方式が無効です。  <br/> |
|TaskCannotModifyProjectSummary = 7031  <br/> |プロジェクトのサマリー タスクを変更できません。  <br/> |
|TaskCannotDeleteProjectSummary = 7032  <br/> |プロジェクトのサマリー タスクを削除できません。  <br/> |
|TaskCannotSetActualCost = 7033  <br/> |タスクの実績コストを設定できません。  <br/> |
|TaskLevelingDelayInvalid = 7034  <br/> |タスクの平準化による延期期間が無効です。  <br/> |
|TaskCannotEditSummary = 7035  <br/> |サマリー タスクを編集できません。  <br/> |
|TaskCannotCreateSubTasksUnderTasksWithAssignments = 7036  <br/> |割り当てがあるタスクの下にサブタスクを作成することはできません。  <br/> |
|TaskCannotDeleteSubProject = 7037  <br/> |タスクの下位プロジェクトを削除できません。  <br/> |
|TaskCannotEditExternal = 7038  <br/> |外部タスクを編集できません。  <br/> |
|TaskCannotDeleteExternal = 7039  <br/> |外部タスクを削除できません。  <br/> |
|TaskLinkCannotDeleteExternal = 7040  <br/> |外部タスクへのリンクを削除できません。  <br/> |
|TaskCannotModifyNullTask = 7041  <br/> |NULL タスクは変更できません。  <br/> |
|TaskCannotModifyLeafTaskWithNoAssignment = 7042  <br/> |割り当てのない末端タスクは変更できません。  <br/> |
|TaskCannotModifyExternalTask = 7043  <br/> |外部タスクを変更できません。  <br/> |
|TaskStatusManagerInvalid = 7044  <br/> |タスクの進捗管理者が無効です。  <br/> |
|TaskLinkCyclicDependency = 7045  <br/> |タスクのリンクに循環依存関係があります。  <br/> |
|TaskCannotCreateOrModifySubTasksUnderTasksWithAssignments = 7046  <br/> |割り当てがあるサマリー タスクの下のサブタスクを作成または変更することはできません。  <br/> |
|TaskLinkCannotEditExternal = 7047  <br/> |外部タスクへのリンクを編集できません。  <br/> |

<a name="pj15_ErrorCodes_Timesheets"></a>

## <a name="table-28-timesheet"></a>表 28 です。 Timesheet 

|タイムシートのエラー コード|説明|
|:-----|:-----|
|TimesheetMaxHourPerDayExceeded = 3201  <br/> |タイムシートの 1 日ごとの最大時間を超過しました。  <br/> |
|TimesheetHoursPerTSLimitExceeded = 3202  <br/> |タイムシートの時間数の制限を超過しました。  <br/> |
|TimesheetUnverifiedTSLineNotAllowed = 3203  <br/> |この場合、未検証のタイムシート行は使用できません。  <br/> |
|TimesheetIncorrectMode = 3204  <br/> |タイムシート モードが無効です。  <br/> |
|TimesheetInvalidApprover = 3205  <br/> |タイムシート承認者が無効です。  <br/> |
|TimesheetFutureReportingNotAllowed = 3206  <br/> |タイムシートに対して将来のアイテムを報告することはできません。  <br/> |
|TimesheetIncorrectPeriod = 3208  <br/> |タイムシート期間が無効です。  <br/> |
|TimesheetPeriodClosed = 3209  <br/> |タイムシート期間が閉じられています。  <br/> |
|TimesheetPendingLines = 3210  <br/> |タイムシート行が保留状態です。  <br/> |
|TimesheetInvalidDateRange = 3211  <br/> |タイムシート日付範囲が無効です。  <br/> |
|TimesheetLineClassDisabled = 3212  <br/> |タイムシートの行分類が無効です。  <br/> |
|TimesheetLineHasNonExistentItem = 3213  <br/> |存在しないアイテムがタイムシート行に含まれています。  <br/> |
|TimesheetLineInvalidStatus = 3214  <br/> |タイムシート行の状態が無効です。  <br/> |

<a name="pj15_ErrorCodes_UserDelegation"></a>

## <a name="table-29-user-delegation"></a>表 29 です。 ユーザーの委任 

|ユーザーの委任のエラー コード|説明|
|:-----|:-----|
|UserDelegationExpired = 43000  <br/> |ユーザーの委任の期限が切れました。  <br/> |
|UserDelegationCannotSelfDelegate = 43001  <br/> |ユーザーは自分自身に対して委任することはできません。  <br/> |
|UserDelegationInvalidDelegate = 43002  <br/> |ユーザーの委任が無効です。  <br/> |
|UserDelegationInvalidUser = 43003  <br/> |ユーザーが委任に対して無効です。  <br/> |
|UserDelegationInvalidDates = 43004  <br/> |ユーザーの委任の日付が無効です。  <br/> |
|UserDelegationCannotDoubleDelegate = 43005  <br/> |2 つの委任を作成することはできません。  <br/> |
|UserDelegationDelegateCannotLogon = 43006  <br/> |ユーザーの代理人が Project Server にログオンできません。  <br/> |
|UserDelegationDelegateIsInactive = 43007  <br/> |ユーザーの委任は非アクティブです。  <br/> |
|UserDelegationInvalidFilter = 43008  <br/> |ユーザーの委任フィルターが無効です。  <br/> |
|UserDelegationUserCannotLogon = 43010  <br/> |ユーザーが Project Server にログオンできません。  <br/> |
|UserDelegationUserIsInactive = 43011  <br/> |ユーザーの委任は非アクティブです。  <br/> |

<a name="pj15_ErrorCodes_Workflow"></a>

## <a name="table-30-workflow"></a>表 30 です。 ワークフロー 

|ワークフローのエラー コード|説明|
|:-----|:-----|
|WorkflowPhasesCannotCreatePhase = 35000  <br/> |ワークフロー フェーズを作成できません。  <br/> |
|WorkflowPhasesCannotUpdatePhase = 35001  <br/> |ワークフロー フェーズを更新できません。  <br/> |
|WorkflowPhasesCannotDeletePhase = 35002  <br/> |ワークフロー フェーズを削除できません。  <br/> |
|WorkflowPhaseNameIsRequired = 35003  <br/> |[PHASE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_NAME.aspx)のワークフローは、必要があります。  <br/> |
|WorkflowStagesCannotCreateStage = 35004  <br/> |ワークフロー ステージを作成できません。  <br/> |
|WorkflowStagesCannotUpdateStage = 35005  <br/> |ワークフロー ステージを更新できません。  <br/> |
|WorkflowStagesCannotDeleteStage = 35006  <br/> |ワークフロー ステージを削除できません。  <br/> |
|WorkflowStagesProjectsInStage = 35007  <br/> |ワークフロー ステージにプロジェクトが存在します。  <br/> |
|WorkflowCannotAccessPDPLibrary = 35008  <br/> |プロジェクト詳細ページ ライブラリにアクセスできません。  <br/> |
|WorkflowInvalidPDPUid = 35009  <br/> |プロジェクト詳細ページの GUID が無効です。  <br/> |
|WorkflowInvalidCustomFieldUid = 35010  <br/> |ユーザー設定フィールドの GUID が無効です。  <br/> |
|WorkflowCustomFieldNotWorkflowControlled = 35011  <br/> |ユーザー設定フィールドはワークフローによって制御されていません。  <br/> |
|WorkflowCustomFieldCannotBeRequiredAndReadOnly = 35012  <br/> |ワークフローのユーザー設定フィールドを必須かつ読み取り専用にすることはできません。  <br/> |
|WorkflowInvalidWorkflowPhaseUid = 35013  <br/> |[PHASE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_UID.aspx)ワークフローが有効ではありません。  <br/> |
|WorkflowInsertWorkflowPhaseNotAllowed = 35014  <br/> |ワークフロー フェーズを挿入できません。  <br/> |
|WorkflowInvalidWorkflowStageUid = 35015  <br/> |[STAGE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_UID.aspx)ワークフローが有効ではありません。  <br/> |
|WorkflowPhaseHasStages = 35016  <br/> |ワークフロー フェーズにステージがあります。  <br/> |
|WorkflowStageNameIsRequired = 35020  <br/> |[STAGE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_NAME.aspx)のワークフローでは、必要があります。  <br/> |
|WorkflowStageAtLeastOnePDPIsRequired = 35021  <br/> |ワークフロー ステージには少なくとも 1 つのプロジェクト詳細ページが必要です。  <br/> |
|WorkflowCannotStartWorkflow = 35100  <br/> |ワークフローを開始できません。  <br/> |
|WorkflowStatusCannotUpdateStatus = 35101  <br/> |ワークフローの状態を更新できません。  <br/> |
|WorkflowOnlyProjectsHaveWorkflow = 35102  <br/> |ワークフローを持つことができるのはプロジェクトのみです。  <br/> |
|WorkflowNoWorkflowsDefined = 35103  <br/> |ワークフローが定義されていません。  <br/> |
|WorkflowInvalidStageForProject = 35104  <br/> |プロジェクトのワークフロー ステージが無効です。  <br/> |
|WorkflowNoWorkflowForProject = 35105  <br/> |プロジェクトにワークフローがありません。  <br/> |
|WorkflowCheckinRequiredAndProjectNotCheckedin = 35106  <br/> |ワークフローを機能させるにはプロジェクトにチェックインする必要があります。  <br/> |
|WorkflowWaitingForRequiredData = 35107  <br/> |ワークフローは必要なデータを待機しています。  <br/> |
|WorkflowFlagCustomFieldsCannotBeRequired = 35108  <br/> |フラグのユーザー設定フィールドをワークフロー内で必須にすることはできません。  <br/> |
|WorkflowCannotChangeWorkflow = 35109  <br/> |ワークフローを変更できません。  <br/> |
|WorkflowWorkflowStatusPDPNotAllowed = 35110  <br/> |ワークフローの状態に関するプロジェクト詳細ページは許可されていません。  <br/> |
|WorkflowInvalidWorkflowStatusPDPUid = 35111  <br/> |ワークフローの状態に関するプロジェクト詳細ページの GUID が無効です。  <br/> |
|WorkflowInvalidStageStatusValue = 35112  <br/> |ワークフロー ステージの状態の値が有効ではありません。 ワークフロー内のステージの状態を設定すると、値だけ**InProgressRequestSent**、 **InProgressRunning**、または[Workflow.StageStatus](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Workflow.StageStatus.aspx)で**InProgressWaiting**ことができます。  <br/> |
|WorkflowCannotCheckinNotify = 35113  <br/> |プロジェクトがチェックインされたことをワークフローに通知できません。  <br/> |
|WorkflowCannotCommitNotify = 35114  <br/> |プロジェクトがプランナーまたはオプティマイザーにコミットされたことをワークフローに通知できません。  <br/> |
|WorkflowExceptionStartingWorkflow = 35115  <br/> |ワークフローの開始時にエラーが発生しました。  <br/> |
|WorkflowStatusPDPMustBeSupplied = 35116  <br/> |ワークフローの状態に関するプロジェクト詳細ページが必要です。  <br/> |
|WorkflowWorkflowProxyAccountNotFound = 35117  <br/> |ワークフローのプロキシ アカウントが見つかりません。  <br/> |
|WorkflowInvalidCurrentStage = 35118  <br/> |ワークフローの現在のステージが無効です。  <br/> |
|WorkflowMultipleStagesInProgress = 35119  <br/> |ワークフロー内に進行中のステージが複数あります。  <br/> |
|WorkflowActivityInvalidArgument = 35120  <br/> |ワークフロー アクティビティが無効な引数を受け取った場合に返されるメッセージ。  <br/> |
|WorkflowMTWConfigurationError = 35121  <br/> |Microsoft Azure のワークフローの構成エラーです。  <br/> |
|EnterpriseProjectTypeInvalidEnterpriseProjectTypeUid = 35200  <br/> |**ENTERPRISE_PROJECT_TYPE_UID**が有効ではありません。  <br/> |
|EnterpriseProjectTypeCannotCreateEnterpriseProjectType = 35201  <br/> |エンタープライズ プロジェクトの種類を作成できません。  <br/> |
|EnterpriseProjectTypeCannotUpdateEnterpriseProjectType = 35202  <br/> |エンタープライズ プロジェクトの種類を更新できません。  <br/> |
|EnterpriseProjectTypeCannotDeleteEnterpriseProjectType = 35203  <br/> |エンタープライズ プロジェクトの種類を削除できません。  <br/> |
|EnterpriseProjectTypeCannotCreateMultipleEnterpriseProjectTypes = 35204  <br/> |複数のエンタープライズ プロジェクトの種類を作成することはできません。  <br/> |
|EnterpriseProjectTypeCannotUpdateMultipleEnterpriseProjectTypes = 35205  <br/> |複数のエンタープライズ プロジェクトの種類を更新することはできません。  <br/> |
|EnterpriseProjectTypeInvalidCreatePDPUid = 35206  <br/> |エンタープライズ プロジェクト テンプレート (EPT) には、関連付けられたプロジェクト詳細ページ (PDP) で、EPT を使用してプロジェクトを作成する必要があります。 EPT がワークフローの場合は、プロジェクト詳細ページ (PDP) が*作成する*タイプではない場合 EPT 検証中にこのエラーが発生します。 他の PDP な種類の*標準*ワークフローに関連するプロジェクトの詳細を表示するためのプロジェクトおよび*ワークフローの状態*を編集します。  <br/> |
|EnterpriseProjectTypeInvalidProjectPlanTemplateUid = 35207  <br/> |[ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID.aspx)が有効ではありません。  <br/> |
|EnterpriseProjectTypeInvalidWorkspaceTemplateName = 35208  <br/> |[ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME.aspx)が有効ではありません。  <br/> |
|EnterpriseProjectTypeInvalidWorkflowAssociationUid = 35209  <br/> |[WORKFLOW_ASSOCIATION_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.WORKFLOW_ASSOCIATION_UID.aspx)が有効ではありません。  <br/> |
|EnterpriseProjectTypeCannotReadWssSettings = 35210  <br/> |SharePoint の設定を読み取れません。  <br/> |
|EnterpriseProjectTypeCannotReadWssLanguagesAndTemplates = 35211  <br/> |SharePoint の言語とサイト テンプレートを読み取れません。  <br/> |
|EnterpriseProjectTypeInvalidDepartmentUid = 35212  <br/> |[DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.DEPARTMENT_UID.aspx)が有効ではありません。  <br/> |
|EnterpriseProjectTypeInvalidUri = 35213  <br/> |[ENTERPRISE_PROJECT_TYPE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.ENTERPRISE_PROJECT_TYPE_UID.aspx)が有効ではありません。  <br/> |
|EnterpriseProjectTypeUriRequiresHttp = 35214  <br/> |エンタープライズ プロジェクトの種類の URI には HTTP プロトコルが必要です。  <br/> |
|EnterpriseProjectTypeCannotDeleteDefault = 35215  <br/> |既定のエンタープライズ プロジェクトの種類は削除できません。  <br/> |
|EnterpriseProjectTypeCannotChangeDefault = 35216  <br/> |既定のエンタープライズ プロジェクトの種類は変更できません。  <br/> |
|EnterpriseProjectTypeHasProjectsCannotDelete = 35217  <br/> |プロジェクトを含んでいるエンタープライズ プロジェクトの種類は削除できません。  <br/> |
|EnterpriseProjectTypeCreatePDPIsRequired = 35218  <br/> |ワークフローのエンタープライズ プロジェクト テンプレート (EPT) には、関連付けられている*作成*の種類のプロジェクト詳細ページ (PDP) で、EPT を使用してプロジェクトを作成する必要があります。 PDP が EPT 定義に含まれていない場合、このエラーが発生します。 他の PDP な種類の*標準*ワークフローに関連するプロジェクトの詳細を表示するためのプロジェクトおよび*ワークフローの状態*を編集します。  <br/> |
|EnterpriseProjectTypeOnlyOneCreatePDPAllowed = 35219  <br/> |EPT 定義は、1 つだけ*を作成する*種類のプロジェクト詳細ページを使用できます。  <br/> |
|EnterpriseProjectTypeHasWorkflowOnlyCreatePDPAllowed = 35220  <br/> |ワークフローのエンタープライズ プロジェクト テンプレート (EPT) には、関連付けられている*作成*の種類のプロジェクト詳細ページ (PDP) で、EPT を使用してプロジェクトを作成する必要があります。 ワークフロー EPT 定義に PDP の別の型の場合、このエラーが発生します。 他の PDP な種類の*標準*ワークフローに関連するプロジェクトの詳細を表示するためのプロジェクトおよび*ワークフローの状態*を編集します。  <br/> |
|EnterpriseProjectTypeInvalidData = 35221  <br/> |エンタープライズ プロジェクトの種類の**WorkflowDataSet**には、無効なデータがあります。  <br/> |
|EnterpriseProjectNoDefaultEnterpriseProjectTypeDefined = 35222  <br/> |エンタープライズ プロジェクトの種類が定義されていません。  <br/> |
|EnterpriseProjectTypeAtLeastOnePDPIsRequired = 35223  <br/> |エンタープライズ プロジェクトの種類には、少なくとも 1 つのプロジェクト詳細ページが必要です。  <br/> |
|EnterpriseProjectTypeWorkflowStatusPDPNotAllowed = 35224  <br/> |エンタープライズ プロジェクトの種類では、ワークフローの状態に関するプロジェクト詳細ページは許可されていません。  <br/> |
|EnterpriseProjectTypeCannotChangeWorkflowAssociation = 35225  <br/> |プロジェクトには既にエンタープライズ プロジェクトの種類 (EPT) があります。プロジェクトの EPT は変更できません。  <br/> |

<a name="pj15_ErrorCodes_WSS"></a>

## <a name="table-31-wssinterop-and-objectlinkprovider-sharepoint-integration"></a>表 31 です。 WssInterop と ObjectLinkProvider (SharePoint の統合)

|SharePoint 統合エラー コード|説明|
|:-----|:-----|
|WSSCreateSiteFailure = 16400  <br/> |プロジェクト ワークスペース用の SharePoint サイトの作成に失敗しました。  <br/> |
|WSSCannotCreateWebWithBlankName = 16401  <br/> |名前が空白の SharePoint Web サイトを作成することはできません。  <br/> |
|WSSWebAlreadyExists = 16402  <br/> |SharePoint Web サイトが既に存在します。  <br/> |
|WSSInvalidProjectUID = 16403  <br/> |SharePoint プロジェクト ワークスペースに対してプロジェクト GUID が無効です。  <br/> |
|WSSProjectAlreadyHasSpWeb = 16404  <br/> |プロジェクトには既に SharePoint ワークスペース サイトがあります。  <br/> |
|WSSWebDoesNotExist = 16405  <br/> |SharePoint Web サイトが存在しません。  <br/> |
|WSSSpWebAlreadyLinkedToProject = 16406  <br/> |SharePoint Web サイトは既にプロジェクトにリンクされています。  <br/> |
|WSSWebHierarchyDoesNotExist = 16407  <br/> |SharePoint Web 階層が存在しません。  <br/> |
|WSSSPWebHasChildren = 16408  <br/> |SharePoint Web には子 Web があります。  <br/> |
|WSSURIInvalidFormat = 16409  <br/> |SharePoint Web URI の形式が無効です。  <br/> |
|WSSSyncReportingDataFailed = 16410  <br/> |SharePoint に関するデータ報告の同期に失敗しました。  <br/> |
|WSSWorkspaceUrlPathTooLong = 16411  <br/> |SharePoint プロジェクト ワークスペースの URL パスが長すぎます。  <br/> |
|WSSWorkspaceNameContainsIllegalChars = 16412  <br/> |SharePoint プロジェクトのサイト名に 1 つまたは複数の文字を使用することはできません。 プロジェクト名を使用することができません:/」: \<\> | , . ' ? \* #  <br/> |
|WSSInvalidWssServerUid = 16413  <br/> |SharePoint サーバー GUID が無効です。  <br/> |
|WSSSyncUsersFailed = 16414  <br/> |Project Server ユーザーを SharePoint に同期させることに失敗しました。  <br/> |
|WSSWrongWebTemplateLCID = 16415  <br/> |SharePoint Web テンプレート ロケール識別子 (言語 ID) が無効です。  <br/> |
|WSSWrongWebTemplate = 16416  <br/> |SharePoint Web テンプレートが無効です。  <br/> |
|WSSWebIsNotProjectWorkspace = 16417  <br/> |SharePoint Web サイトはプロジェクト ワークスペースではありません。  <br/> |
|WSSWebCannotStartOrEndOnPeriod = 16418  <br/> |SharePoint Web 名の先頭または末尾にはピリオドを使用できません。  <br/> |
|WSSCannotDeleteSiteCollection = 16419  <br/> |Web サイト コレクションを削除できません。  <br/> |
|WSSListUidInvalid = 16420  <br/> |SharePoint リスト GUID が無効です。  <br/> |
|WSSSyncDataSetListUidMismatch = 16421  <br/> |SharePoint リストの GUID では、リストの同期の**データセット**内の GUID が一致しません。  <br/> |
|WSSSyncDataSetMissingProjectSettingsRow = 16422  <br/> |SharePoint と同期するための**データセット**には、プロジェクトの設定の行がありません。  <br/> |
|WSSSyncDataSetTaskMappingsNotAllowed = 16423  <br/> |SharePoint と同期するためは、**データセット**内のタスクのマッピングは使用できません。  <br/> |
|WSSSyncDataSetWssListUidEmpty = 16424  <br/> |SharePoint リストの GUID は SharePoint と同期するための**データセット**の空です。  <br/> |
|WSSSyncDataNotFound = 16425  <br/> |SharePoint との同期処理でデータが不足しています。  <br/> |
|WSSSyncCriticalDataValidationError = 16426  <br/> |SharePoint との同期処理で重大なデータ検証エラーが発生しました。  <br/> |
|WSSSyncSharePointListNotAccessibleError = 16427  <br/> |SharePoint リストにアクセスできません。  <br/> |
|WSSSyncInvalidEntityUids = 16428  <br/> |SharePoint との同期に使用するエンティティ GUID が無効です。  <br/> |
|WSSSyncInvalidSyncData = 16429  <br/> |SharePoint の同期処理に無効なデータが含まれています。  <br/> |
|WSSSyncSPSummaryTaskAssignedToResourceError = 16430  <br/> |SharePoint の同期処理に、リソースに割り当てられたサマリー タスクが含まれています。  <br/> |
|WSSSyncInsufficientPermissionsToCreateWinUser = 16431  <br/> |SharePoint との同期処理を行うときに、Windows ユーザーを作成するための十分な権限がありませんでした。  <br/> |
|WSSSyncNoDefaultValueForCustomField = 16432  <br/> |SharePoint の同期処理で、ユーザー設定フィールドに既定値が設定されていません。  <br/> |
|WSSOLPCreateLinkFailure = 18000  <br/> |SharePoint オブジェクト リンク プロバイダー用のリンクの作成に失敗しました。  <br/> |
|WSSOLPDeleteWebObjectLinkError = 18001  <br/> |SharePoint オブジェクト リンク プロバイダー内の Web オブジェクト リンクの削除エラー。  <br/> |
|WSSInvalidPermissionsToWssList = 18002  <br/> |SharePoint リストに関する権限が無効です。  <br/> |
|WSSWebIsNotUnderDefaultCollection = 18003  <br/> |SharePoint Web が既定のコレクションに含まれていません。  <br/> |
|WSSWorkspaceUrlIsNotUnderPrimaryCollection = 18004  <br/> |指定したワークスペースの url は、project server のこのインスタンスに関連付けられているサイト コレクションではありません。 これが現在のアクセス許可モードが必要です。  <br/> |
|WSSWorkspacesMustBeRestrictedToDefaultCollection = 18005  <br/> |現在の権限モードでは、ワークスペースを既定のサイト コレクションに制限する必要があります。  <br/> |

<a name="pj15_ErrorCodes_ASMXExample"> </a>

## <a name="error-code-example-for-asmx"></a>ASMX のエラー コードの例

エラーの一覧を取得するには、PSI メソッドを呼び出すと例外を取得する場合に、 [Microsoft.Office.Project.Server.Library.PSClientError](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.aspx)クラスのコンス トラクターに**SoapException**オブジェクトを渡します。 **PSErrorInfo**アレイでエラー情報を格納し、次の例のように、エラーを列挙し、 [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx)を使用できます。 
  
> [!NOTE]
> すべての情報をする必要があります**PSErrorInfo**オブジェクトは含まれません。 たとえば、 **Resource.CheckOutResources**リソースのいずれかが既にチェック アウトを使用する場合**PSErrorInfo**はリソースをチェック アウトすることはできませんが、リソースの名前または GUID が含まれていないエラーの原因を示しています。 ASMX ベースのアプリケーションの詳細情報を取得する方法、 [CheckOutResources](https://msdn.microsoft.com/library/WebSvcResource.Resource.CheckOutResources.aspx)を参照してください。 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using System.Web.Services.Protocols;
using System.Windows.Forms;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch (SoapException ex)
{
    string errAttributeName;
    string errAttribute;
    string errMess = "".PadRight(30, '=') + "\r\n" + "Error: " + "\r\n";
    PSLibrary.PSClientError error = new PSLibrary.PSClientError(ex);
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\n" + ex.Message.ToString() + "\r\n";
        errMess += "".PadRight(30, '=') + "\r\nPSCLientError Output:\r\n \r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName +
                       ": " + errAttribute;
        }
        errMess += "\r\n".PadRight(30, '=');
    }
    MessageBox.Show(errMess, "Error", MessageBoxButtons.OK,
        MessageBoxIcon.Error);
}
```

<a name="pj15_ErrorCodes_WCFExample"> </a>

## <a name="error-code-example-for-wcf"></a>WCF のエラー コードの例

エラーの一覧を取得するには、WCF ベースのアプリケーションの PSI メソッドを呼び出す場合に、 **System.ServiceModel.FaultException**を取得する場合に、 **FaultException**オブジェクトから、 **PSClientError**オブジェクトを抽出できます。 **PSErrorInfo**アレイでエラー情報を格納し、ASMX の前の例のように、エラーを列挙し、 [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx)を使用できます。 
  
```cs
using System;
using System.Text;
using System.ServiceModel;
using System.Xml;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch(FaultException fault)
{
    // Use the WCF FaultException, because the ASMX SoapException does not 
    // exist in a WCF-based application.
    WriteFaultOutput(fault);
}
// Get a PSClientError object from the WCF FaultException object, and
// then display the exception details and each error in the PSClientError stack.
private static void WriteFaultOutput(FaultException fault)
{
    string errAttributeName;
    string errAttribute;
    string errOut;
    string errMess = "".PadRight(30, '=') + "\r\n"
        + "Error details: " + "\r\n";
    PSLibrary.PSClientError error = GetPSClientError(fault, out errOut);
    errMess += errOut;
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\r\n".PadRight(30, '=') + "\r\nPSClientError output:\r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName
                + ": " + errAttribute;
        }
    }
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine(errMess);
    Console.ResetColor();
}
/// <summary>
/// Extract a PSClientError object from the ServiceModel.FaultException,
/// for use in output of the GetPSClientError stack of errors.
/// </summary>
/// <param name="e"></param>
/// <param name="errOut">Shows that FaultException has more information 
/// about the errors than PSClientError has. FaultException can also contain 
/// other types of errors, such as failure to connect to the server.</param>
/// <returns>PSClientError object, for enumerating errors.</returns>
public static PSLibrary.PSClientError GetPSClientError(FaultException e, 
                                                        out string errOut)
{
    const string PREFIX = "GetPSClientError() returns null: ";
    errOut = string.Empty;
    PSLibrary.PSClientError psClientError = null;
    if (e == null)
    {
        errOut = PREFIX + "Null parameter (FaultException e) passed in.";
        psClientError = null;
    }
    else
    {
        // Get a ServiceModel.MessageFault object.
        var messageFault = e.CreateMessageFault();
        if (messageFault.HasDetail)
        {
            using (var xmlReader = messageFault.GetReaderAtDetailContents())
            {
                var xml = new XmlDocument();
                xml.Load(xmlReader);
                var serverExecutionFault = xml["ServerExecutionFault"];
                if (serverExecutionFault != null)
                {
                    var exceptionDetails = serverExecutionFault["ExceptionDetails"];
                    if (exceptionDetails != null)
                    {
                        try
                        {
                            errOut = exceptionDetails.InnerXml + "\r\n";
                            psClientError = 
                                new PSLibrary.PSClientError(exceptionDetails.InnerXml);
                        }
                        catch (InvalidOperationException ex)
                        {
                            errOut = PREFIX + "Unable to convert fault exception info ";
                            errOut += "a valid Project Server error message. Message: \n\t";
                            errOut += ex.Message;
                            psClientError = null;
                        }
                    }
                    else
                    {
                        errOut = PREFIX + "The FaultException e is a ServerExecutionFault, "
                            + "but does not have ExceptionDetails.";
                    }
                }
                else
                {
                    errOut = PREFIX + "The FaultException e is not a ServerExecutionFault.";
                }
            }
        }
        else // No detail in the MessageFault.
        {
            errOut = PREFIX + "The FaultException e does not have any detail.";
        }
    }
    errOut += "\r\n" + e.ToString() + "\r\n";
    return psClientError;
}

```

<br/>

**FaultException**オブジェクトは、 **PSClientError**オブジェクトにデータを Project Server に接続するための障害などのエラーの他の種類を含めることができます。 前の例では、 **GetPSClientError**メソッドの_errOut_パラメーターには、追加情報が表示されます。 たとえば、 [QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx)メソッドで**CreateProject4Department**のコード サンプルには、 **ProjectCustomFields**テーブルのプロパティを設定するときにエラーを作成する方法を説明するコメントが含まれています。 アプリケーションを実行すると、 _errOut_パラメーターには、 **errinfo**要素と (ここではコンソールの出力から書式設定された) その他のデータが含まれます。 
  
```XML
==============================
Error details:
<errinfo xmlns="">
  <dataset name="ProjectDataSet">
    <table name="ProjectCustomFields">
      <row CUSTOM_FIELD_UID="976d3bd9-95ff-40a2-a938-960c410b0341">
        <error id="11704" name="CustomFieldInvalidTypeColumnFilledIn" 
               uid="aa8a2fab-9262-422f-b022-ca1cb12bc75f"></error>
        <error id="11713" name="CustomFieldRequiredValueNotProvided" 
               uid="dc2e2156-86e9-4aac-bede-d07dc44dfedc"></error>
      </row>
    </table>
  </dataset>
</errinfo>
System.ServiceModel.FaultException`1[SvcProject.ServerExecutionFault]: 
ProjectServerError(s) LastError=CustomFieldRequiredValueNotProvided Instructions: 
Pass this into PSClientError constructor to access all error information 
(Fault Detail is equal to SvcProject.ServerExecutionFault).
============================
PSClientError output:
CustomFieldInvalidTypeColumnFilledIn
============================
PSClientError output:
CustomFieldRequiredValueNotProvided
```

<a name="pj15_ErrorCodes_AR"> </a>

## <a name="see-also"></a>関連項目

- [Microsoft.Office.Project.Server.Library.PSErrorID](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSErrorID.aspx)
- [WebSvcProject.PSErrorID](https://msdn.microsoft.com/library/WebSvcProject.PSErrorID.aspx)
- [プロジェクトの概念と操作方法に関する記事](project-conceptual-and-how-to-articles.md)
- [SQL Server プロファイラー](http://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx)
- [プロジェクトの Server 2010: どのような予期しないを取得する場合に期待する](http://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx)
- [ULS ビューアー](http://www.codeproject.com/Articles/458052/ULS-Log-Viewer)
    

