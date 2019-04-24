---
title: 夏時間に合わせてプログラムにより予定表を調整することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: このトピックでは、春と秋の間の期間を DST 期間と呼びます。
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316955"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>夏時間に合わせてプログラムにより予定表を調整することについて

多くの国では、夜の夏時間を延長することで夏時間 (DST) を守っています。 これは、通常、スプリングを1時間に設定してから、秋に時計を1時間後に設定することによって行われます。 このトピックでは、春と秋の間の期間を DST 期間と呼びます。 ほとんどの国には、DST の開始時と終了時に固有の規制があります。 dst の期間の日付は年単位で変更され、ユーザーは dst 規則が変更されるたびに Microsoft Outlook の予定表を更新する必要があります。 
  
windows Vista 以降のバージョンの windows を使用している場合、または windows 自動更新が有効になっている場合は、DST の変更による影響を受けない可能性があります。 それ以外の場合は、Windows 用の DST 更新プログラムをインストールする必要があります。 更新プログラムが自動的にインストールされるのか、IT 部門が代行するのか、または自宅ユーザーであるかに関係なく、dst 期間中に発生する既存の予定の中には、Windows の dst 更新プログラムのインストール後に誤った時刻が表示される場合があります。. これは、定期的な予定と単一インスタンスの予定の両方に当てはまります。 これらの予定を更新して、outlook、outlook Web App、およびコラボレーションデータオブジェクト (CDO) に基づくアプリケーションで、これらを正しく表示する必要があります。 DST のために予定表を再配置するという理由で、正しく表示されていない予定を予定表に更新します。
  
Outlook には、ユーザーおよび Exchange Server 用のツールが用意されており、管理者は予定表を再配置することができます。 outlook では、outlook ユーザー用のタイムゾーンデータ更新ツールが提供されています。 このツールを使用すると、ユーザーは自分の予定表を更新できます。 exchange Server には、管理者が exchange 予定表更新ツールを提供しており、outlook ツールをすべてのユーザーに幅広く展開し、各ユーザーが outlook ツールを正しく実行していることを確認することによって、問題が発生しないようにすることができます。
  
タイムゾーンデータ更新ツールまたは管理者が Exchange 予定表更新ツールを実行するためにユーザーに依存するだけでなく、サードパーティ製の MAPI クライアントソフトウェア開発者は dll、tzmovelib.h をダウンロードできます。 このアセンブリを使用すると、開発者は Outlook と Exchange Server が予定表の再配置ツールで使用するのと同じ api を使用できます。 

次のリストは、カレンダーの再配置 api を示しています。
  
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
    
予定表の再配置 api を使用して予定の再配置ツールを作成するには、次の手順を実行します。
  
1. **IOlkApptRebaser:: BeginEnumerateAppointments**と**IOlkApptRebaser:: EndEnumerateAppointments**を使用して、再配置する候補の予定を検索します。 必要に応じて、再配置する予定を決定するための情報をユーザーに提示します。 または、MAPI または Outlook オブジェクトモデルを使用して、 **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**を解析することにより、予定の時刻と定期的な情報を調べます。プロパティと**PidLidAppointmentTimeZoneDefinitionRecur**プロパティ。 
    
2. **hrcreateapptrebaser**、 **IOlkApptRebaser:: beginrebaseappointments**、および**IOlkApptRebaser:: endrebaseappointments**を使用して、予定を再配置します。 
    
、tzmovelib.h アセンブリを入手するには、OutlookTimeZoneMoveLibRedist 再頒布可能パッケージと、tzmovelib.h ヘッダーファイルを Outlook にダウンロードします。 [2010: 補助参照再配布可能なインストーラーと、予定表を再配置するためのヘッダーファイル](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b). このダウンロードは、outlook 2010 以降のバージョンの outlook で使用できます。 OutlookTimeZoneMoveLibRedist は、、tzmovelib.h アセンブリファイルを C:\Program Files\MsExTmz. にインストールします。 サードパーティ製の予定表の再配置アプリケーションは、インストーラ OutlookTimeZoneMoveLibRedist のみを再配布することができ、アセンブリ、、tzmovelib.h、またはその他の抽出されたコンポーネントをインストーラーとは別に再配布することはできません。
  
## <a name="see-also"></a>関連項目

- [バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)
- [夏時間のヘルプとサポートセンター](https://support.microsoft.com/gp/cp_dst)
- [Exchange 予定表更新ツールを使用して夏時間に対処する方法](https://support.microsoft.com/kb/941018)
- [[方法] Microsoft Office Outlook 用タイムゾーンデータ更新ツールを使用してタイムゾーンの変更に対処する](https://support.microsoft.com/kb/931667)

