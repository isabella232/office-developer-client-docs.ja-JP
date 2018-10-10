---
title: DBEngine.IniPath プロパティ (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1bb594ad9866785db3d12f114f6be0eccbbe2289
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477740"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniPath プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

Microsoft Access データベース エンジン用の値が含まれた Windows レジストリ キーに関する情報を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。IniPath

*式***DBEngine**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

Windows レジストリを使用して Microsoft Access データベース エンジンを構成できます。このレジストリを使用すると、インストール可能な ISAM DLL などのオプションを設定できます。

このオプションを有効にするには、 **IniPath** プロパティを設定してから、アプリケーションで他の DAO コードを呼び出す必要があります。この設定の有効範囲は使用するアプリケーションに限定され、範囲を変更するにはアプリケーションを再起動する必要があります。

また、レジストリを使用すると、インストール可能な ISAM データベース ドライバーの初期化パラメーターを用意できます。たとえば、Paradox バージョン 4.0 を使用するには、 **IniPath** プロパティを、該当するパラメーターが含まれたレジストリの一部の値に設定します。

このプロパティは、いずれかの HKEY を認識\_ローカル\_マシンまたは HKEY\_ローカル\_ユーザーです。 HKEY が既定ではルート キーを指定しない場合は\_ローカル\_マシンです。

