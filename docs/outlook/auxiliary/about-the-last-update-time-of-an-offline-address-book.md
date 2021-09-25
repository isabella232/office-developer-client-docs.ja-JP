---
title: オフライン アドレス帳の最終更新時刻について
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: オフライン アドレス帳 (OAB) は、Outlook ユーザーが、切断された状態情報にアクセスできるディレクトリからグローバル アドレス一覧 (GAL) およびその他のアドレス帳からを提供します。
ms.openlocfilehash: 57904298c0265585e4613c4f2a7f4dd466cedd7b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592831"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a>オフライン アドレス帳の最終更新時刻について

オフライン アドレス帳 (OAB) は、Outlook ユーザーが、切断された状態情報にアクセスできるディレクトリからグローバル アドレス一覧 (GAL) およびその他のアドレス帳からを提供します。Outlook がオフラインのアクセスを提供する Exchange サーバーからダウンロードするアドレス帳のコピーすることをお勧めします。
  
Exchange 管理者は、ユーザーがオフラインで作業できるようにするには、どのアドレス帳を選択できます。アドレス帳のコピーを作成するには、Exchange は、ファイルを圧縮、および、ローカル共有に配置する新しい OAB ファイルが生成されます。Outlook の構成方法によっては、Outlook は、切断された状態で Web サイトからまたはクライアント コンピューターにパブリック フォルダーのいずれかを使用して OAB ファイルをダウンロードします。Outlook は定期的にチェックされ、更新された OAB がダウンロードされます。
  
ユーザーの OAB へのオフライン アクセスを提供する outlook ソリューションでは、OAB が Exchange サーバーから最後に更新されたときに検出する必要があります。 OAB の最終更新時刻を検索するには、ソリューションは、Windows レジストリで次のエントリを使用できます: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB 最終変更時間** 。このレジストリ エントリの種類は、 **REG_BINARY** です。データは、サイズが 8 バイトです。前回ダウンロードされた OAB ファイルの Exchange サーバーからクライアント コンピューターに世界協定時刻 (UTC) の値を指定する 64 ビット [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx)構造体にデータを変換できます。 
  
## <a name="see-also"></a>関連項目

- [Managing Offline Address Books](https://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)

