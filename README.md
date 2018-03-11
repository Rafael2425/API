
//MAIN

package me.rafael2425.smallapi;

import java.util.ArrayList;
import java.util.List;

import org.bukkit.Bukkit;
import org.bukkit.entity.Player;
import org.bukkit.plugin.java.JavaPlugin;

public class Main extends JavaPlugin {
	public static Main m;
	public List<Player> staffs = new ArrayList<>();
	
	@Override
	public void onEnable() {
		m = this;
		Bukkit.getConsoleSender().sendMessage("");
		Bukkit.getConsoleSender().sendMessage("             §a§lSmall-API");
		Bukkit.getConsoleSender().sendMessage("      §fAPI carragada com sucesso.");
		Bukkit.getConsoleSender().sendMessage("");
		Bukkit.getConsoleSender().sendMessage("        §b/vinish - §fAtivado");
		Bukkit.getConsoleSender().sendMessage("        §b/limparchat - §fAtivado");
		Bukkit.getConsoleSender().sendMessage("           §b/cs - §fAtivado");
		Bukkit.getConsoleSender().sendMessage("");
		Bukkit.getServer().getPluginManager().registerEvents(new Eventos(), this);;
		getCommand("limparchat").setExecutor(new Limparchat());
		getCommand("vanish").setExecutor(new Vanish());
		Mensagens();
	}
	public void Mensagens(){
		Bukkit.getScheduler().scheduleSyncRepeatingTask(this, new Runnable() {
			int indeddx = 1;
			@Override
			public void run() {
				if (indeddx == 1){
					Bukkit.broadcastMessage("");
					Bukkit.broadcastMessage("                 §3§lSMALL NETWORK");
					Bukkit.broadcastMessage("  §bVocê sabia que em breve seremos uma network?");
					Bukkit.broadcastMessage("  §bFique atento no nosso twittter para saber mais!");
					Bukkit.broadcastMessage("");
					indeddx = 2;
					return;
				}
				if (indeddx == 2){
					Bukkit.broadcastMessage("");
					Bukkit.broadcastMessage("                 §3§lSMALL NETWORK");
					Bukkit.broadcastMessage("   §bEvite colocar senhas fáceis e não ultilize");
					Bukkit.broadcastMessage("       §ba mesma senha em outros servidores.");
					Bukkit.broadcastMessage("");
					indeddx = 3;
					return;
				}
				if (indeddx == 3){
					Bukkit.broadcastMessage("");
					Bukkit.broadcastMessage("                 §3§lSMALL NETWORK");
					Bukkit.broadcastMessage("  §bQuer saber de tudo que acontece no servidor?");
					Bukkit.broadcastMessage("         §bNos siga no twitter: §6@SmallLand_.");
					Bukkit.broadcastMessage("");
					indeddx = 4;
					return;
				}
				if (indeddx == 4){
					Bukkit.broadcastMessage("");
					Bukkit.broadcastMessage("                 §3§lSMALL NETWORK");
					Bukkit.broadcastMessage("     §bViu algum hack atrapalhando o seu jogo?");
					Bukkit.broadcastMessage(" §bUltilize o comando /reportar <nick> para reporta-lo.");
					Bukkit.broadcastMessage("");
					indeddx = 5;
					return;
				}
				if (indeddx == 5){
					Bukkit.broadcastMessage("");
					Bukkit.broadcastMessage("                 §3§lSMALL NETWORK");
					Bukkit.broadcastMessage(" §bTem um canal no youtube e quer receber vantagens?");
					Bukkit.broadcastMessage("    §bDigite o comando §6/youtube §epara saber mais.");
					Bukkit.broadcastMessage("");
					indeddx = 1;
					return;
				}
				
			}
		}, 0, 120*20);

	}

}
