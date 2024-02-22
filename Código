import tkinter as tk
from tkinter import messagebox

class ControleAtendimentoApp:
    def __init__(self, root):
        self.root = root
        self.root.title("Controle de Atendimento")

        # Variáveis para armazenar os dados do cliente
        self.nome = tk.StringVar()
        self.telefone = tk.StringVar()
        self.experiencia = tk.StringVar()
        self.sessoes = tk.IntVar()
        self.resultado = tk.StringVar()
        self.tempo = tk.IntVar()
        self.intercorrencia = tk.StringVar()
        self.bronze = tk.StringVar()
        self.areas = []

        # Widgets para o cadastro do cliente
        tk.Label(root, text="Nome:").grid(row=0, column=0)
        tk.Entry(root, textvariable=self.nome).grid(row=0, column=1)
        tk.Label(root, text="Telefone:").grid(row=1, column=0)
        tk.Entry(root, textvariable=self.telefone).grid(row=1, column=1)
        tk.Button(root, text="Capturar Foto", command=self.capturar_foto).grid(row=2, columnspan=2)

        # Widgets para o preenchimento da ficha
        tk.Label(root, text="Experiência:").grid(row=3, column=0)
        tk.Radiobutton(root, text="Sem experiência", variable=self.experiencia, value="Sem experiência").grid(row=3, column=1)
        tk.Radiobutton(root, text="Com experiência", variable=self.experiencia, value="Com experiência").grid(row=3, column=2)

        tk.Label(root, text="Número de Sessões:").grid(row=4, column=0)
        tk.Entry(root, textvariable=self.sessoes).grid(row=4, column=1)
        tk.Label(root, text="Resultado:").grid(row=5, column=0)
        tk.Entry(root, textvariable=self.resultado).grid(row=5, column=1)
        tk.Label(root, text="Tempo (meses):").grid(row=6, column=0)
        tk.Entry(root, textvariable=self.tempo).grid(row=6, column=1)

        tk.Label(root, text="Intercorrência:").grid(row=7, column=0)
        tk.Radiobutton(root, text="Com intercorrência", variable=self.intercorrencia, value="Com intercorrência").grid(row=7, column=1)
        tk.Radiobutton(root, text="Sem intercorrência", variable=self.intercorrencia, value="Sem intercorrência").grid(row=7, column=2)
        tk.Label(root, text="Descrição da Intercorrência:").grid(row=8, column=0)
        self.descricao_intercorrencia = tk.Text(root, height=4, width=30)
        self.descricao_intercorrencia.grid(row=8, column=1)

        tk.Label(root, text="Bronzeamento:").grid(row=9, column=0)
        tk.Radiobutton(root, text="Bronze Muito", variable=self.bronze, value="Bronze Muito").grid(row=9, column=1)
        tk.Radiobutton(root, text="Bronze Pouco", variable=self.bronze, value="Bronze Pouco").grid(row=9, column=2)
        tk.Radiobutton(root, text="Bronze Normal", variable=self.bronze, value="Bronze Normal").grid(row=9, column=3)

        tk.Label(root, text="Áreas:").grid(row=10, column=0)
        self.virilha_var = tk.IntVar()
        self.axilas_var = tk.IntVar()
        self.perna_inteira_var = tk.IntVar()
        self.meia_perna_var = tk.IntVar()
        self.contorno_barba_var = tk.IntVar()

        tk.Checkbutton(root, text="Virilha", variable=self.virilha_var).grid(row=10, column=1)
        tk.Checkbutton(root, text="Axilas", variable=self.axilas_var).grid(row=10, column=2)
        tk.Checkbutton(root, text="Perna Inteira", variable=self.perna_inteira_var).grid(row=10, column=3)
        tk.Checkbutton(root, text="Meia Perna", variable=self.meia_perna_var).grid(row=10, column=4)
        tk.Checkbutton(root, text="Contorno Barba", variable=self.contorno_barba_var).grid(row=10, column=5)

        # Botão para salvar e exibir os dados
        tk.Button(root, text="Salvar", command=self.salvar_dados).grid(row=11, columnspan=6)

    def capturar_foto(self):
        # Implemente a lógica para capturar a foto aqui
        messagebox.showinfo("Capturar Foto", "Implemente a captura de foto aqui")

    def salvar_dados(self):
        # Obter os dados do cliente
        nome = self.nome.get()
        telefone = self.telefone.get()
        experiencia = self.experiencia.get()
        sessoes = self.sessoes.get()
        resultado = self.resultado.get()
        tempo = self.tempo.get()
        intercorrencia = self.intercorrencia.get()
        descricao_intercorrencia = self.descricao_intercorrencia.get("1.0", "end-1c")
        bronze = self.bronze.get()
        
        # Obter as áreas selecionadas
        areas_selecionadas = []
        if self.virilha_var.get():
            areas_selecionadas.append("Virilha")
        if self.axilas_var.get():
            areas_selecionadas.append("Axilas")
        if self.perna_inteira_var.get():
            areas_selecionadas.append("Perna Inteira")
        if self.meia_perna_var.get():
            areas_selecionadas.append("Meia Perna")
        if self.contorno_barba_var.get():
            areas_selecionadas.append("Contorno Barba")

        # Exibir os dados
        messagebox.showinfo("Dados do Cliente", f"Nome: {nome}\nTelefone: {telefone}\nExperiência: {experiencia}\nNúmero de Sessões: {sessoes}\nResultado: {resultado}\nTempo: {tempo} meses\nIntercorrência: {intercorrencia}\nDescrição da Intercorrência: {descricao_intercorrencia}\nBronzeamento: {bronze}\nÁreas Selecionadas: {', '.join(areas_selecionadas)}")

root = tk.Tk()
app = ControleAtendimentoApp(root)
root.mainloop()
