---
title: 技術的要件
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: このトピックでは、サポートされているプログラミング言語、COM の可視性とメソッドの戻り値の型の要件、および Outlook Social Connector (.osc) プロバイダ拡張 DLL の詳細について説明します。
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329156"
---
# <a name="technical-requirements"></a>技術的要件

このトピックでは、サポートされているプログラミング言語、COM の可視性とメソッドの戻り値の型の要件、および Outlook Social Connector (.osc) プロバイダ拡張 DLL の詳細について説明します。 
  
## <a name="programming-language-and-com-requirements"></a>プログラミング言語と COM の要件

.osc プロバイダーを作成するには、visual C# または visual Basic などのマネージ言語または visual C++ などのアンマネージ言語を使用します。 COM で認識可能な DLL コンポーネントを作成できる任意のツールを使用して、.osc プロバイダーを開発できます。 マネージ言語またはアンマネージ言語を使用してプロバイダーを開発する場合は、プロバイダーインストールパッケージのダウンロードサイズと依存関係を考慮する必要があります。
  
.osc プロバイダーは、次のように定義されているように、COM から参照可能である必要があります。
  
- インストール後は、COM の自己登録または regsvr32 を使用して、.osc プロバイダーを登録する必要があります。
    
- .osc プロバイダ DLL の COM 登録は、そのプロバイダーを HKCU または HKLM の下に登録します。 
    
- プロバイダーの ProgID は、に登録`HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`されています。
    
- マネージ言語で開発された .osc プロバイダーは、COM に表示されます。
    
- .osc プロバイダーは、Windows レジストリに値を追加する必要があります。これは、プロバイダー DLL がシングルスレッドアパートメント (STA) とマルチスレッドアパートメント (MTA) スレッドモデルの両方をサポートしていることを示します。 COM スレッドモデルの詳細については、「 [OLE スレッディングモデルの説明と働き](https://support.microsoft.com/kb/150777)」を参照してください。
    
.osc プロバイダ拡張性のメソッドは、 **string**や**bool**などのプリミティブ型を返す必要があります。 **文字列**の戻り値は、そのプロバイダー拡張機能のスキーマ定義に準拠している必要があります。 戻り値としてサポートされているのは XML のみです。 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>.osc プロバイダ拡張 DLL の詳細

.osc プロバイダ拡張機能をサポートするコンポーネントは、.osc プロバイダ拡張 DLL です。 サードパーティの開発者は、これらの機能拡張インターフェイスを使用して、.osc プロバイダ dll を作成できます。 次のリストは、.osc プロバイダ拡張 DLL の詳細を示しています。
  
- 機能拡張 DLL ファイル名: 指定した dll
    
- 機能拡張 DLL のフレンドリ名: Microsoft Outlook Social Provider の拡張性
    
- 機能拡張 DLL のメジャーバージョン: 15.0
    
- Extensibiilty DLL TypeLib バージョン: 1.1
    
## <a name="miscellaneous-technical-information"></a>その他の技術情報

JavaScript Object Notation (JSON) は、.osc プロバイダ拡張モデルではサポートされていません。
  
XML パーサーに依存関係はありません。 .osc プロバイダーは、microsoft xml Core Services (MSXML) などの Office に付属する xml パーサーを使用して、microsoft .net Framework に組み込まれている xml 解析機能を使用するか、サードパーティの xml パーサーを使用できます。 
  
## <a name="see-also"></a>関連項目

- [プロバイダーを開発するためのベストプラクティス](best-practices-for-developing-a-provider.md)  
- [プロバイダーを開発するための簡単な手順](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーを展開する](deploying-a-provider.md)  
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

