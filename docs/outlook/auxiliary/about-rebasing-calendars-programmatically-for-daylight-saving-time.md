---
title: 夏時間に合わせてプログラムにより予定表を調整することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: このトピックでは、春と秋の間のこの期間を DST 期間と呼ばれます。
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316955"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>夏時間に合わせてプログラムにより予定表を調整することについて

多くの国では、夜間の夏時間が長くなるので、クロックを進めることによって夏時間 (DST) が観測されます。 これは通常、春に 1 時間先に時計を設定し、秋に 1 時間戻して設定することで行われます。 このトピックでは、春と秋の間のこの期間を DST 期間と呼ばれます。 ほとんどの国では、DST の開始および終了に関する独自の規制があります。 DST 期間の日付は年ごとに変更される可能性があります。また、ユーザーは DST 規制が変更される度に Microsoft Outlookカレンダーを更新する必要があります。 
  
Vista 以降のバージョンの Windows を使用Windows、または Windows 自動更新を有効にしている場合は、DST の変更の影響を受けない可能性があります。 それ以外の場合は、DST 更新プログラムをインストールする必要Windows。 更新プログラムが自動的にインストールされるか、IT 部門によって、またはホーム ユーザーとして自動的にインストールされるかに関係なく、DST 期間中に発生する一部の既存の予定は、Windows の DST 更新プログラムがインストールされた後に正しく表示されません。 これは、定期的な予定と単一インスタンスの予定の両方に当てはまる。 これらの予定を更新して、Outlook、Outlook Web App、およびコラボレーション データ オブジェクト (CDO) に基づくアプリケーションで正しく表示する必要があります。 DST が理由で予定表に正しく表示されていない予定を更新すると、予定表の再予約と呼ばれることがあります。
  
Outlookユーザーと管理者向けツールExchange Server、管理者が予定表を再ベースするためのツールを提供します。 Outlookユーザー向けタイム ゾーン データ更新ツールOutlook提供します。 このツールを使用すると、ユーザーは自分の予定表を更新できます。 Exchange Server Exchange カレンダー更新ツールは、管理者が Outlook ツールをすべてのユーザーに広く展開し、各ユーザーが Outlook ツールを正しく実行することで生じにくい問題を回避するのに役立ちます。
  
ユーザーがタイム ゾーン データ更新ツールを実行するか、管理者が Exchange 予定表更新ツールを実行するだけでなく、サードパーティの MAPI クライアント ソフトウェア開発者は DLL、Tzmovelib.dll をダウンロードできます。 このアセンブリを使用すると、開発者はカレンダーの再OutlookツールExchange Server同じ API を使用できます。 

次の一覧は、予定表の再バーズ API を示しています。
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
予定表の再バーズ API を使用して予定の再処理ツールを作成するには、次の手順を使用します。
  
1. **IOlkApptRebaser::BeginEnumerateAppointments** および **IOlkApptRebaser::EndEnumerateAppointments** を使用して、リベースの候補である予定を検索します。 必要に応じて、ユーザーがリベースする予定を決定できる情報を提示します。 または、MAPI または Outlook オブジェクト モデルを使用して **、PidLidAppointmentTimeZoneDefinitionStartDisplay、PidLidAppointmentTimeZoneDefinitionEndDisplay、****および PidLidAppointmentTimeZoneDefinitionRecur** プロパティを解析して、予定の時間と繰り返し情報を調べてください。  
    
2. 予定を再ベース化するには **、HrCreateApptRebaser** **、IOlkApptRebaser::BeginRebaseAppointments、****および IOlkApptRebaser::EndRebaseAppointments** を使用します。 
    
Tzmovelib.dll アセンブリを取得するには、Outlook [2010](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)の OutlookTimeZoneMoveLibRedist.exe 再頒布可能インストーラーと Tzmovelib.h ヘッダー ファイルをダウンロードします。 このダウンロードは、2010 Outlook以降のバージョンのバージョンでOutlook。 OutlookTimeZoneMoveLibRedist.exe C:\Program Files\MsExTmz にTzmovelib.dllアセンブリ ファイルをインストールします。 サード パーティ製の予定表の再分散アプリケーションでは、インストーラー 、OutlookTimeZoneMoveLibRedist.exe のみを再配布できます。また、アセンブリ、Tzmovelib.dll、または他の抽出されたコンポーネントをインストーラーとは別に再配布する必要があります。
  
## <a name="see-also"></a>関連項目

- [バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)
- [夏時間のヘルプとサポート センター](https://support.microsoft.com/gp/cp_dst)
- [カレンダー更新ツールを使用して夏時間に対処Exchange方法](https://support.microsoft.com/kb/941018)
- [タイム ゾーン データ更新ツールを使用してタイム ゾーンの変更に対処するMicrosoft Office Outlook](https://support.microsoft.com/kb/931667)

