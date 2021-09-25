---
title: 技術的要件
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: このトピックでは、サポートされているプログラミング言語、COM 可視性とメソッドの戻り値の型の要件、および Outlook Social Connector (OSC) プロバイダー拡張 DLL の詳細について説明します。
ms.openlocfilehash: 5d5ca78c7ff1e328257b7e645731e76a2e6e5633
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604061"
---
# <a name="technical-requirements"></a>技術的要件

このトピックでは、サポートされているプログラミング言語、COM 可視性とメソッドの戻り値の型の要件、および Outlook Social Connector (OSC) プロバイダー拡張 DLL の詳細について説明します。 
  
## <a name="programming-language-and-com-requirements"></a>プログラミング言語と COM の要件

OSC プロバイダーは、Visual C# や Visual Basic などの管理言語、または Visual C++ などの管理されていない言語を使用して作成できます。 COM に表示される DLL コンポーネントを作成できる任意のツールを使用して、OSC プロバイダーを開発できます。 管理言語または管理されていない言語を使用してプロバイダーを開発する決定は、プロバイダー インストール パッケージのダウンロード サイズと依存関係を考慮する必要があります。
  
OSC プロバイダーは、次の定義に従って COM に表示されている必要があります。
  
- インストール後、COM 自己登録または regsvr32 を使用して OSC プロバイダーを登録する必要があります。
    
- OSC プロバイダー DLL の COM 登録は、HKCU または HKLM の下でプロバイダーを登録します。 
    
- プロバイダーの ProgID は 、 の下に登録されています  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` 。
    
- マネージ言語で開発された OSC プロバイダーは、COM に表示されます。
    
- OSC プロバイダーは、プロバイダー DLL がシングル スレッド アパートメント (STA) とマルチスレッド アパートメント (MTA) スレッド モデルの両方をサポートしているという値を Windows レジストリに追加する必要があります。 COM スレッド モデルの詳細については [、「DESCRIPTIONs and Workings of OLE Threading Models」を参照してください](https://support.microsoft.com/kb/150777)。
    
OSC プロバイダーの機能拡張のメソッドは、string や bool などのプリミティブ型 **を****返す必要があります**。 特定 **の文字列** 戻り値は、OSC プロバイダーの機能拡張のスキーマ定義に準拠している必要があります。 戻り値としてサポートされているのは XML のみです。 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>OSC プロバイダー拡張 DLL の詳細

OSC プロバイダーの機能拡張をサポートするコンポーネントは、OSC プロバイダー拡張 DLL です。 サードパーティの開発者は、これらの機能拡張インターフェイスを使用して OSC プロバイダー DLL を構築できます。 次の一覧は、OSC プロバイダー拡張 DLL の詳細を示しています。
  
- 拡張 DLL ファイル名: socialprovider.dll
    
- 拡張 DLL の表示名: Microsoft Outlook ソーシャル プロバイダーの機能拡張
    
- 拡張 DLL メジャー バージョン: 15.0
    
- Extensibiilty DLL TypeLib バージョン: 1.1
    
## <a name="miscellaneous-technical-information"></a>その他の技術情報

JAVAScript オブジェクト表記 (JSON) は、OSC プロバイダー拡張モデルではサポートされていません。
  
XML パーサーには依存関係はありません。 OSC プロバイダーは、Office MSXML (Microsoft XML Core Services )などの Office に含まれる XML パーサーを使用したり、Microsoft .NET Framework に組み込まれている XML 解析機能を使用したり、サードパーティの XML パーサーを使用できます。 
  
## <a name="see-also"></a>関連項目

- [プロバイダーの開発に関するベスト プラクティス](best-practices-for-developing-a-provider.md)  
- [プロバイダーを開発するためのラーニング手順](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーの展開](deploying-a-provider.md)  
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

