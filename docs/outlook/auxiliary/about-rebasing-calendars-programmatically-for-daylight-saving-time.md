---
title: 夏時間のプログラムを使用して予定表を再配置について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: このトピックでは、春と秋の間には、この期間を DST の期間と呼びます。
ms.openlocfilehash: 4787b2143b3f5d1f0400524f0da82e19e2cbed8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799295"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>夏時間のプログラムを使用して予定表を再配置について

多くの国では、夜が長くなります (夏時間) できるように、時計を進めることで夏時間 (DST) を観察します。 、春に今後 1 時間時計を設定することによってこれは、通常、秋の 1 時間にバックアップの時計の設定。 このトピックでは、春と秋の間には、この期間を DST の期間と呼びます。 ほとんどの国では、DST の開始時と終了時の独自の規制があります。 DST の期間の日付から 1 年に 1 年を変更できます、ユーザーする必要があります更新、Microsoft Outlook の予定表毎回 DST 規則を変更することです。 
  
Windows Vista は、Windows のバージョンを使用するかどうかまたは後で、Windows の自動更新が有効になっていることもすることがありますいない影響を受ける DST の変更。 それ以外の場合、Windows の DST 更新プログラムをインストールする必要があります。 DST の期間中に発生するいくつかの既存の予定かどうか、更新プログラムはお客様に代わって、IT 部門では、または自分でホーム ユーザーは、自動的にインストールに関係なく Windows の DST 更新プログラムをインストールした後に誤った時刻を表示可能性があります。. これは、定期的な予定と単独の予定の場合は true。 Outlook、Outlook Web App では、およびコラボレーション データ オブジェクト (CDO) をベースとするアプリケーションで正しく表示するのにはこれらの予定を更新する必要があります。 DST のために、カレンダーが正しく表示されている予定を更新すると、予定表を再配置と呼ばれます。
  
Outlook には、ユーザー用のツールが用意されていて、Exchange Server には、カレンダーを再設定する管理者用のツールが用意されています。 Outlook は、Outlook ユーザーのタイム ゾーン データ更新ツールを提供します。 このツールでは、ユーザーが独自のカレンダーを更新できます。 Exchange Server には、管理者が Outlook ツールをすべてのユーザーに広く展開するために発生する問題を回避し、各ユーザーが Outlook ツールを正しく実行するかどうかを確認するのには Exchange 予定表更新ツールが用意されています。
  
タイム ゾーン データ更新ツールを実行するユーザーまたは管理者は、Exchange 予定表更新ツールの実行に依存している、だけでなくサードパーティの MAPI クライアントのソフトウェア開発者は、DLL、Tzmovelib.dll をダウンロードできます。 このアセンブリを使用すると、開発者は、Outlook と Exchange Server を使用してツールを再配置の予定表に共通の Api を使用できます。 

Api を再配置する予定表を次に示します。
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Api を再配置する予定表を使用して予定の再配置ツールを作成するには、次の手順を使用できます。
  
1. 候補を再配置するため、予定を検索するのにには、 **IOlkApptRebaser::BeginEnumerateAppointments**と**IOlkApptRebaser::EndEnumerateAppointments**を使用します。 必要に応じて、再配置するには、対象となる予定を決定するユーザーを有効にする情報を表示します。 また、MAPI または Outlook オブジェクト モデルを使用して、 **PidLidAppointmentTimeZoneDefinitionStartDisplay**、 **PidLidAppointmentTimeZoneDefinitionEndDisplay**を解析することによって、予定の時間と定期的なアイテムの情報を確認するには**PidLidAppointmentTimeZoneDefinitionRecur**のプロパティを選択します。 
    
2. 予定を再配置するのにには、 **HrCreateApptRebaser**、 **IOlkApptRebaser::BeginRebaseAppointments**、および**IOlkApptRebaser::EndRebaseAppointments**を使用します。 
    
Tzmovelib.dll アセンブリを取得するには、「OutlookTimeZoneMoveLibRedist.exe の再頒布可能なインストーラーと、Tzmovelib.h ヘッダー ファイルでの使用」をダウンロードしていますください。 [Outlook 2010: 補助型の参照の再頒布可能なインストーラーと再配置の予定表のヘッダー ファイル](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b). このダウンロードは、Outlook 2010 およびそれ以降のバージョンの Outlook の動作します。 OutlookTimeZoneMoveLibRedist.exe は、C:\Program Files\MsExTmz で Tzmovelib.dll のアセンブリ ファイルをインストールします。 そのサードパーティ製のカレンダー アプリケーションを再配置は、OutlookTimeZoneMoveLibRedist.exe、インストーラーのみを再配布でき、アセンブリ、Tzmovelib.dll、またはインストーラーから個別に抽出されたその他のコンポーネントを再配布する必要があります注意してください。
  
## <a name="see-also"></a>関連項目

- [バイナリ プロパティをストリームに永続化の TZDEFINITION について](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [TZDEFINITION 構造体を読み取るためのバイナリのプロパティからのストリームを解析します。](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [TZREG 構造体を読み取るためのバイナリのプロパティからのストリームを解析します。](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)
- [夏時間のヘルプとサポート センター](http://support.microsoft.com/gp/cp_dst)
- [Exchange 予定表更新ツールを使用して夏時間に対応する方法](http://support.microsoft.com/kb/941018)
- [Microsoft Office Outlook 用タイム ゾーン データ更新ツールを使用してタイム ゾーンの変更に対処する方法](http://support.microsoft.com/kb/931667)

