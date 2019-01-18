---
title: Outlook PIA のインストールと参照
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718204"
---
# <a name="installing-and-referencing-the-outlook-pia"></a>Outlook PIA のインストールと参照

Outlook 管理アドインで PIA の情報を取り込むには、その前にグローバル アセンブリ キャッシュ (GAC) に Outlook プライマリ相互運用機能アセンブリ (PIA) をインストールしておく必要があります。 既定では、PIA は開発コンピューターに Office をインストールするときに自動的にインストールされます。 ただし、PIA を別途インストールする必要がある場合は、「[Office ソリューションを開発できるようにコンピューターを構成する](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017)」を参照してください。


> [!NOTE] 
> Office PIA をインストールするには開発コンピューターで管理者でなければなりません。

インストール後、Visual Studio を使用して管理オブジェクトを作成している場合、[ Microsoft Outlook 15.0 Object Library] コンポーネントへの参照を追加できます。その後、オブジェクト ブラウザーの [ **Microsoft.Office.Interop.Outlook**] 名前空間の下に、Outlook オブジェクト モデル内のオブジェクトに対応する名前の、PIA 内の管理インターフェイスが表示されます。

## <a name="see-also"></a>関連項目

- [Office プライマリ相互運用機能アセンブリのインストール](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [Outlook PIA のアーキテクチャ](architecture-of-the-outlook-pia.md)

