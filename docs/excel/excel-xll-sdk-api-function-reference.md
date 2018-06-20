---
title: Excel XLL SDK API �֐����t�@�����X
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798874"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Excel XLL SDK API �֐����t�@�����X

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel 2013 XLL SDK �ɂ́AXLL �̋L�q����������邽�߂ɐ݌v���ꂽ�t���[�����[�N ���C�u�����̃\�[�X �t�@�C���� 2 �̃T���v�� �v���W�F�N�g (Example �� Generic) ���܂܂�܂��B 
  
���̃Z�N�V�����ł́A���̊֐����t�@�����X��񋟂��܂��B
  
- XLL �t�@�C�����Ăяo�����Ƃ̂ł��� Excel �R�[���o�b�N�B
    
- Microsoft Excel ���������� XLL �R�[���o�b�N�B
    
- �T���v���ƃt���[�����[�N�̃v���W�F�N�g�̎�v�ȋ@�\�B
    
## <a name="sample-projects"></a>サンプル プロジェクト

Excel 2013 XLL SDK �ɂ́A���̃T���v�� �v���W�F�N�g�̃\�[�X �t�@�C���� Microsoft Visual Studio �̃v���W�F�N�g �t�@�C�����܂܂�܂��B
  
- **フレームワーク**プロジェクト (`SAMPLES\FRAMEWRK\`) FRAMEWRK.lib で、他の XLL プロジェクトにリンクすることができます、ライブラリにビルドできるプロジェクトが含まれています。 ライブラリには、多くの関数や Xll に簡単に記述するためのツールが含まれています。 このライブラリは、ヘッダー ファイル FRAMEWRK.h を使用して、連携して、他のプロジェクトの両方で使用されます。
    
- **例**プロジェクト (`SAMPLES\EXAMPLE\`)、xll ファイルの EXAMPLE.xll をビルドできるプロジェクトが含まれています。 Xll ファイルには、フレームワーク ライブラリを使用し、XLL アドイン インターフェイスなどの機能の**xlAutoOpen**の実装の例の多くの例が含まれています。
    
- **汎用的な**プロジェクト (`SAMPLES\GENERIC\`)、xll ファイルの GENERIC.xll をビルドできるプロジェクトが含まれています。 Xll ファイルはいくつかの例の関数とコマンドの例を示します、独自の Xll を記述するための開始点です。
    
## <a name="in-this-section"></a>このセクションの内容

- [�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)
  
- [C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md)
  
- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)
  
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)
  
- [�ėp DLL �̊֐�](functions-in-the-generic-dll.md)
  
- [Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>�֘A����

- [Excel �ł� C API ��g�p�����v���O���~���O](programming-with-the-c-api-in-excel.md)
  
- [Excel XLL �̊J��](developing-excel-xlls.md)

