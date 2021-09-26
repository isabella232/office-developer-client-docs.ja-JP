---
title: Outlook PIA のインストールと参照
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a18e781e99b29bef464a96d9ae2c7927b7a196ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583094"
---
# <a name="installing-and-referencing-the-outlook-pia"></a>Outlook PIA のインストールと参照

Outlook 管理アドインで PIA の情報を取り込むには、その前にグローバル アセンブリ キャッシュ (GAC) に Outlook プライマリ相互運用機能アセンブリ (PIA) をインストールしておく必要があります。 既定では、PIA は開発コンピューターに Office をインストールするときに自動的にインストールされます。 ただし、PIA を別途インストールする必要がある場合は、「[Office ソリューションを開発できるようにコンピューターを構成する](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017)」を参照してください。


> [!NOTE] 
> Office PIA をインストールするには開発コンピューターで管理者でなければなりません。

インストール後、Visual Studio を使用して管理オブジェクトを作成している場合、[ Microsoft Outlook 15.0 Object Library] コンポーネントへの参照を追加できます。その後、オブジェクト ブラウザーの [ **Microsoft.Office.Interop.Outlook**] 名前空間の下に、Outlook オブジェクト モデル内のオブジェクトに対応する名前の、PIA 内の管理インターフェイスが表示されます。

## <a name="see-also"></a>関連項目

- [Office プライマリ相互運用機能アセンブリのインストール](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [Outlook PIA のアーキテクチャ](architecture-of-the-outlook-pia.md)

