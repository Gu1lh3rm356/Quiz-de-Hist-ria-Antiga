# Questionário Histórico
Tente acertar todas as questões. Se acertar todas,vc é legáu
import sys

def executar_quiz():
    # Lista de perguntas atualizada com 9 questões
    perguntas = [
        {
            "pergunta": "Qual o país de origem do comandante Adolf Hitler?",
            "alternativas": {
                "A": "Alemanha",
                "B": "Áustria",
                "C": "Polônia",
                "D": "Hungria"
            },
            "correta": "B"
        },
        {
            "pergunta": "Qual o nome do povo localizado no oriente médio?",
            "alternativas": {
                "A": "Persas",
                "B": "Egípcios",
                "C": "Otomanos",
                "D": "Árabes"
            },
            "correta": "D"
        },
        {
            "pergunta": "Qual era o nome do primeiro presidente da República do Brasil?",
            "alternativas": {
                "A": "Dom Pedro I",
                "B": "Marechal Deodoro da Fonseca",
                "C": "Marechal Floriano Peixoto",
                "D": "Juscelino Kubitschek"
            },
            "correta": "B"
        },
        {
            "pergunta": "Qual foi considerada a guerra mais longa da história?",
            "alternativas": {
                "A": "A Reconquista",
                "B": "Guerra de Independência dos Estados Unidos",
                "C": "Guerra Sino Japonesa",
                "D": "Guerra do Paraguai"
            },
            "correta": "A"
        },
        {
            "pergunta": "Quanto tempo durou a guerra mais longa?",
            "alternativas": {
                "A": "359 Anos",
                "B": "534 Anos",
                "C": "781 Anos",
                "D": "836 Anos"
            },
            "correta": "C"
        },
        {
            "pergunta": "Quando a Alemanha ficou independente (Unificação Alemã)?",
            "alternativas": {
                "A": "13/03/1894",
                "B": "18/01/1871",
                "C": "07/09/1822",
                "D": "11/11/1918"
            },
            "correta": "B"
        },
        {
            "pergunta": "Qual o nome da maior operação militar da história?",
            "alternativas": {
                "A": "Plano Schlieffen",
                "B": "Operação Barbarossa",
                "C": "Blitzkrieg",
                "D": "Operação Overlord"
            },
            "correta": "B"
        },
        {
            "pergunta": "Quantos soldados tinham na Operação Barbarossa?",
            "alternativas": {
                "A": "3.8 milhões",
                "B": "4.6 milhões",
                "C": "2.1 milhões",
                "D": "5.2 milhões"
            },
            "correta": "A"
        },
        {
            "pergunta": "Quanto tempo durou a guerra mais rápida da história?",
            "alternativas": {
                "A": "Entre 38 e 45 minutos",
                "B": "Cerca de 2 horas",
                "C": "Exatamente 1 dia",
                "D": "Apenas 6 dias"
            },
            "correta": "A"
        }
        # Você pode adicionar novas perguntas aqui seguindo o mesmo formato acima
    ]

    pontuacao = 0

    print("========================================")
    print("      BEM-VINDO AO QUIZ DE HISTÓRIA     ")
    print("========================================\n")

    for i, item in enumerate(perguntas, 1):
        print(f"Pergunta {i}: {item['pergunta']}")
        for letra, texto in item["alternativas"].items():
            print(f"  {letra}) {texto}")
        
        while True:
            resposta = input("\nSua resposta (A, B, C ou D): ").strip().upper()
            if resposta in item["alternativas"]:
                break
            print("Opção inválida! Por favor, escolha A, B, C ou D.")

        if resposta == item["correta"]:
            print("\nResposta CORRETA!\n")
            pontuacao += 1
        else:
            print(f"\nResposta INCORRETA. A alternativa certa era a ({item['correta']}).\n")
        
        print("-" * 40)

    print("\n========================================")
    print("             FIM DO JOGO                ")
    print(f" Você acertou {pontuacao} de {len(perguntas)} pergunta(s).")
    print("========================================")

if __name__ == "__main__":
    executar_quiz()
